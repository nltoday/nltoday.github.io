---
layout: post
title: "Understanding Different Load Balancing Schemes"
date: 2024-02-06 02:48:45 +0000
categories: "Art"
excerpt_image: https://www.researchgate.net/publication/274007923/figure/fig4/AS:294661710204934@1447264234651/Classification-of-load-balancing-solutions.png
image: https://www.researchgate.net/publication/274007923/figure/fig4/AS:294661710204934@1447264234651/Classification-of-load-balancing-solutions.png
---

Load balancing refers to the distribution of network traffic or processing power across multiple servers, computers, or other resources to maximize throughput, minimize response time, and avoid overload. This helps make computing systems and resources highly scalable and ensures continuous availability of the system even in case of failure of individual components. There are several different load balancing schemes employed by enterprises to distribute workloads efficiently.
## [Even Task Distribution or Round Robin Scheme](https://yt.io.vn/collection/ager) 
One of the simplest and commonly used load balancing scheme is the even or round robin scheme. Here each incoming task or request is distributed sequentially in a circular fashion among the servers in the cluster. So if we have four servers - Server 1, Server 2, Server 3 and Server 4 - the first request would go to Server 1, second to Server 2, third to Server 3, fourth to Server 4 and so on in a rotating manner. This ensures **equal workload distribution** across servers. 
However, the limitation of this approach is that it doesn't account for the varying processing capabilities or workload of different tasks. All tasks are assumed to require equal effort which may not always be the case. One task requiring more resources than others can end up overloading a server despite even distribution of tasks.
### Leveraging Server Capacities

![](https://www.wisdomgeek.com/wp-content/uploads/2021/01/load-balancing-1024x582.png)
## **Weighted Task Distribution Scheme**
To overcome the limitation of not considering varying server capacities, weighted task distribution scheme accounts for differing capabilities of servers. Here servers are assigned weights based on their relative capacities and tasks are distributed among them proportional to these weights. 
For example, if we have three servers with capacities of 1x, 2x and 3x respectively, the distribution ratio would be 1:2:3. So for every 4 tasks that arrive, server 1 would get 1 task, server 2 would get 2 tasks and server 3 would get 3 tasks. This ensures servers with higher capacities receive more tasks while still maintaining an overall balanced distribution.
### Maintaining Session State 
## **Sticky Session Load Balancing**
All the previous schemes assumed independent request processing without consideration for session state. However, many applications require maintaining session-specific data across multiple related requests from a user. Sticky session load balancing addresses this by binding the entire session of a user to the same server.
In this scheme, when the first request of a new session arrives it is routed to a server. All subsequent requests part of the same user session will be directed to the same server till the session ends. 
This prevents loss of session data but can result in **uneven workload distribution** as sessions have varying lengths and resource needs. Longer sessions tied to a single server can cause overloading while others have spare capacity.
### Queue-Based Dynamic Distribution
## **Even Size Task Queue Distribution Scheme**  
To leverage the benefits of weighted distribution while maintaining session affinity, the even size task queue distribution scheme uses a **queue-based dynamic approach**. 
Here incoming tasks are placed in processing queues associated with each server based on their current capacities. Servers with higher available capacities are assigned more tasks from the queue. As tasks get completed, space opens in the queues allowing new tasks to be inserted while maintaining **near equal queue sizes**.
This accounts for both differing server capabilities and varying task efforts more accurately. Overloaded servers see fewer new assignments allowing their queues to clear up. New sessions are tied to a server based on its queue size rather than routing all session requests to a single machine.
## **DNS-Based Load Balancing**
A simpler approach is to leverage Domain Name System or DNS for load distribution. Here the domain is configured to round-robin map to multiple IP addresses of load balanced servers. When clients lookup the domain, they will be returned different IP addresses over multiple requests in a rotating manner. 
Subsequent requests from the client would go to the initially resolved address itself till the DNS entry is cached. This provides a basic form of load balancing without requiring client-side support. However, it has limitations since tasks aren't dynamically distributed based on real-time system loads. Changes also require DNS propagation delays.
## **Hierarchy and Geolocation-Aware Schemes**
For **massively scalable systems**, distributed load balancing is implemented across multiple tiers with geographical awareness. Large enterprises often employ a hierarchy of load balancers - with **regional load balancers** fronting **local data center load balancers**. 
Content like images, videos etc. are hosted on geographically distributed edge servers close to users for low latency. Application servers are load balanced regionally. Database queries are pooled at the center. Real-time analytics help route requests intelligently based on current traffic patterns and server capacities.
This brings immense scalability and fault-tolerance. Outages impact small local regions instead of the entire system. Adaptive schemes sense demand shifts and autoscale resources on demand. Geolocation routing optimizes content delivery based on user locations.
## **Hybrid Approaches** 
In practice, most large-scale systems employ a hybrid of the above load balancing techniques based on application needs. For example, a webshop could use sticky sessions for user carts on the front-end while load balancing product APIs on backend with a weighted queue scheme. A CDN may use DNS and edge server locational awareness. 
Proper load testing helps identify bottlenecks to design the right hybrid technique. Advanced solutions also provide capabilities like session replication, graceful server shutdown, health monitoring etc. Load balancers thus play a pivotal role in architecting robust and scalable distributed systems.
![Understanding Different Load Balancing Schemes](https://www.researchgate.net/publication/274007923/figure/fig4/AS:294661710204934@1447264234651/Classification-of-load-balancing-solutions.png)