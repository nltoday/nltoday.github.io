---
layout: post
title: "Performing Updates in Apache Hive"
date: 2024-01-17 06:42:36 +0000
categories: "News"
excerpt_image: https://i.ytimg.com/vi/Ods-zDnTWxs/maxresdefault.jpg
image: https://i.ytimg.com/vi/Ods-zDnTWxs/maxresdefault.jpg
---

Apache Hive provides SQL syntax and capabilities for querying and analyzing large datasets stored in distributed storage such as Apache Hadoop's HDFS. While Hive has traditionally focused on analytics use cases involving SELECT queries, modern versions now support more transactional workloads through ACID (Atomicity, Consistency, Isolation, Durability) features for DML operations like INSERT, UPDATE, and DELETE. Let's take a closer look at how to perform updates and upserts in Hive.
## Enabling ACID Support
Before Hive 0.14, updates were not supported natively and workarounds like using intermediate tables were required. To enable ACID support, a minimum Hive version of 0.14 or higher is needed. Additionally, the table's file format must be ORC and its properties must be configured with 'transactional'=true. 
The ORC file format provides row-level updates while maintaining data compression and performance. Setting 'transactional'=true marks the table as transactional so DML statements are written to transaction logs rather than directly to data files. While not strictly required, tables should also use [clustering by](https://store.fi.io.vn/collection/allain) and bucketing to improve concurrency and scalability of updates. 
Several configuration parameters also need adjusting to fully enable ACID features in Hive. Setting hive.support.concurrency to true activates locking and isolation between concurrent transactions. Setting hive.enforce.bucketing to true enforces that tables use bucketing. And setting hive.exec.dynamic.partition.mode to nonstrict avoids failures on partition inserts and updates.
## Performing Updates
Once ACID is configured, the standard SQL UPDATE statement can be used to modify existing rows in Hive tables. The WHERE clause identifies which rows to update based on a column value match. For example:
```sql
UPDATE customers 
SET name = 'Jane Doe'
WHERE id = 1001;
```
This would change the name field to 'Jane Doe' for the row where the id is 1001. 
Updates in Hive operate at the partition level rather than row-level for better performance. So updates should target partitions using filters on partition columns when possible. Functions like CURRENT_DATE can help generate dynamic partition filters. 
Transactions are used behind the scenes to ensure atomicity, isolation, and consistency of updates. Concurrency issues are avoided through row-level locks managed by the transaction manager. Compaction cleans up redundant data files after transactions complete.
## Handling Upserts
An upsert, or merge, operation allows inserting new rows or updating existing rows in a single statement. Since Hive does not support a standard MERGE statement, different approaches are used:
### Staging Table Method
One way is to use a staging table to hold new and changed records. An INSERT statement adds these records to the staging table. A join between the main and staging tables identifies records to update versus insert. INSERT OVERWRITE then moves the results to the main table:
```sql 
INSERT OVERWRITE TABLE customers 
SELECT coalesce(c.col1, s.col1) 
FROM customers c
FULL OUTER JOIN staging_customers s
ON c.id = s.id;
```

![](https://data-flair.training/blogs/wp-content/uploads/sites/2/2016/06/Apache-Hive-Introduction-Tutorial-Training.jpg)
### Hudi Integration
[Hudi](https://hudi.apache.org/) is an open source project that provides upsert capabilities for Hive tables. It indexes data to support efficient merge operations and handles updates at the file/record level behind the scenes. This avoids full rewrites and improves performance over the staging table approach.
### HBase Integration 
Another option is to use Hive's integration with HBase, a column-oriented NoSQL database. HBase natively supports record-level updates so it can efficiently handle upserts. Aggregation queries are then pulled back into Hive for analysis. This splits transactional and analytical workloads across systems.
In summary, Hive now has built-in ACID transactional functionality for updates and integrates with tools like Hudi to efficiently handle upserts on large datasets. With the right configuration, Apache Hive can support both batch ETL/ELT workflows and transactional workloads on Hadoop.
## Handling Partitions in Updates
When updating partitioned tables in Hive, it's important to target partitions using filters on the partition columns. This allows updates to operate more efficiently at the partition granularity rather than scanning and updating the entire table.
Use cases like incrementing counters or updating recent records are good candidates for partition-level updates. The partition value can be dynamically determined using functions in the WHERE clause filter. 
For example, to update all records for today's date:
```sql
UPDATE partitioned_table
SET field = 'new value'
WHERE date_partition = CURRENT_DATE;
```
Hive also supports dynamically adding and deleting partitions with statements like ALTER TABLE ADD/DROP PARTITION. So for incremental loads, new partitions can be added and their records updated in a single workflow.
Proper partitioning and targeted partition updates/filters optimize update performance in Hive. The distributed execution engine can then efficiently parallelize the work across partitions on the cluster.
## Streaming Updates with Kafka
For near real-time updates, Apache Hive can integrate with streaming platforms like Apache Kafka. Changes captured by producers in Kafka topics can be consumed and applied to Hive tables using tools like Kubernetes Operators and Apache Spark Structured Streaming.
A common workflow is to write updates from applications to Kafka, then have a streaming job pull those events and apply them to a transactional Hive table using Spark SQL. The table acts as the system of record while still allowing querying of historical data.
For high volume updates, streaming to non-transactional file formats like Parquet may be preferable over Hive tables for better throughput. The data can periodically flush to ORC-formatted transactional tables in Hive for queryability and consistent presence. 
Systems like Kappa Architecture handle both batch and stream processing efficiently at scale. With proper tuning and partitioning, Hive can act as the analytical data store for streaming workloads with low latency requirements.
This covers some of the main techniques for updating and upserting data in Apache Hive on Hadoop distributions. Let me know if any part needs more explanation or if you have additional questions!
![Performing Updates in Apache Hive](https://i.ytimg.com/vi/Ods-zDnTWxs/maxresdefault.jpg)