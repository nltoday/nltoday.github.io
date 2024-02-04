---
layout: post
title: "A Comprehensive Guide to Binary Coded Decimal and Packed Decimal Formats"
date: 2023-11-04 15:51:28 +0000
categories: "News"
excerpt_image: https://i.ytimg.com/vi/8sEUY-PBfaM/maxresdefault.jpg
image: https://i.ytimg.com/vi/8sEUY-PBfaM/maxresdefault.jpg
---

Packed decimal and binary coded decimal (BCD) are data encoding schemes that were commonly used in earlier computer systems to represent decimal numbers in a space efficient manner while maintaining human readability. Though replaced by simpler binary representations for most use cases today, understanding these legacy formats provides valuable historical context. This guide seeks to comprehensively explain packed decimal, binary coded decimal, and their applications.
## Representing Numbers in Early Computers
Early computers lacked hardware support for decimal arithmetic and instead worked natively with binary representations. However, many applications like accounting, inventory, and banking required storing and displaying decimal numbers for human readability. Several techniques were developed to bridge this gap, with [BCD](https://store.fi.io.vn/womens-cute-boston-terrier-american-flag-usa-patriotic-dog-lover-v-neck-t-shirt/women&) and **packed decimal** becoming popular choices. 
BCD encodes each decimal digit as a unique 4-bit pattern, allowing the number to be reconstructed in decimal form. Though only 40% efficient compared to binary, BCD maintained the decimal place and was simple to decode for output. Packed decimal improved density by packing two BCD digits into a single byte, at the cost of more complex encoding and decoding.
### The Case for Efficiency 
Mainframes in the 1960s-70s had very limited memory compared to modern standards. Storing data in an efficient format was critical. While BCD was human-readable, it wasted 3 out of every 4 bits. Engineers noticed the extra "nibble" in each byte was unused and devised packed decimal to store two numbers per byte. This doubled density with **minimal extra processing**.

![](http://ecomputernotes.com/images/thumb587-BCD-Codes-8a4868af3bd5bd92c448b0ff26d4ae08.jpg)
### Representing Fractional Values
BCD could represent fractional values cleanly by encoding the decimal place. However, packed decimal lacked space for a radix marker. Systems instead fixed the radix at a known position, avoiding floating point's precision issues while fitting **large monetary values** in small integers. Four bytes stored under $1 million with two-cent precision.
## Unpacking the Formats
Let's examine packed and unpacked BCD encodings in more detail:
### Packed Decimal Encoding
Packed decimal packs two decimal digits into one byte, using the upper and lower four bits. The number 123 would be encoded as `0001 0011 0010 0011`. This format was highly efficient for storage while retaining decimal values.
### Unpacked BCD Encoding 
In contrast, unpacked or "zoned" BCD dedicates one byte per digit. 123 would require three bytes encoded as `0000 0001 0010 0011`. Though bulkier, it was easier for humans to read and for software to process than packed format.
### Historical Context 
While called "packed decimal" by IBM, these formats conformed to the IEEE standard for BCD. Though inefficient by modern standards, packed decimal achieved IBM's goals of human readability, decimal arithmetic, and efficient data storage decades before floating point hardware.
In summary, packed and unpacked BCD/decimal formats were ingenious solutions that bridged the gap between decimal numbers meaningful to humans and binary representations inside computers. Though superseded, their historical impact was enormous.
## Applications of Packed Formats 
Packed decimal saw widespread use wherever decimal values were important, like business applications:
### Financial Transactions and Accounting
Banking, invoicing, accounting all required storing monetary values precisely. Packed decimal excelled at this by reserving specific bit patterns for currency amounts.
### Inventory Management 
Tracking quantities of inventory items in decimal units was a natural application. Legacy systems still rely on packed formats for compatibility. 
### Date and Time Record Keeping
Dates are fundamentally decimal values and packed representations were ideal for storing event times and calendar information efficiently. 
### EDI and Data Exchange Standards 
Electronic data interchange (EDI) schemas often defined packed decimal as the encoding for monetary and quantitative fields to ensure consistent interpretation across systems.
In these domains and more, packed BCD remained dominant for decades thanks to its balanced treatment of human and machine numeric representation. Its efficient legacy lives on even as systems evolve.
In conclusion, packed decimal and BCD formats were ingenious solutions that maximized early computer resources for storage of decimal numbers. Though obsolete today, their historical impact was tremendous in bridging the gap between human and machine numerical representation. Understanding their role provides valuable context on numerical computing progress.

![A Comprehensive Guide to Binary Coded Decimal and Packed Decimal Formats](https://i.ytimg.com/vi/8sEUY-PBfaM/maxresdefault.jpg)