---
layout: post
title: "Understanding Binary Coded Decimal (BCD)"
date: 2024-03-02 01:57:04 +0000
categories: "Drawing"
excerpt_image: http://ecomputernotes.com/images/thumb587-BCD-Codes-8a4868af3bd5bd92c448b0ff26d4ae08.jpg
image: http://ecomputernotes.com/images/thumb587-BCD-Codes-8a4868af3bd5bd92c448b0ff26d4ae08.jpg
---

Digital data storage has evolved dramatically over the decades as computers have become more advanced. Early computer systems employed clever encoding schemes like binary coded decimal (BCD) to store numeric values efficiently given the limited storage capacity of the time. Let's examine BCD encoding and how it enabled the mainframe computers of the mid-20th century to manage numbers.
### Packed and Unpacked BCD 
BCD represents each decimal digit with a unique 4-bit binary pattern, wasting some bits but allowing straightforward conversion between numeric and character displays. Two common BCD formats were "packed," storing two digits per byte, and "unpacked," using one byte per digit. Packed BCD economized on space but complicated math. Unpacked aligned with character encodings like EBCDIC for easy output but consumed more bytes. For applications involving small numbers and displaying results, packed BCD struck a good balance of space and simplicity.

![](https://i.ytimg.com/vi/8sEUY-PBfaM/maxresdefault.jpg)
### The Origins and Purpose of BCD
At the core, BCD is a simple encoding that maps each decimal digit 0-9 to a distinct 4-bit value. This preserves the numeric meaning when moving between binary and character representations. Early computers lacked efficient floating point arithmetic and needed solutions for storing fractional values. BCD with an implied decimal provided a way to encode decimal numbers literally as sequences of digits. While inefficient compared to native binary, BCD served numerical applications well given the constraints of mid-century hardware. 
### How BCD Addressed Numeric Storage Needs
Storing fixed-point values directly in binary risked losing precision or wasting space. Floating point brought challenges too in the era before standardized formats. BCD provided an intuitive intermediate format: numbers appeared as familiar decimal strings yet used binary under the hood. With packed storage reducing overhead, BCD enabled applications in commerce and science demanding high-fidelity encoding of numeric quantities. Its digit-based structure also made printed output straightforward via character codes. BCD fulfilled primary numeric storage needs until hardware advanced.
### The Role of Packed vs Unpacked BCD
The packed BCD format was highly space-efficient, encoding two decimal digits per byte. This dense encoding facilitated storage and transmission of modest-sized values like monetary amounts. Unpacked BCD aligned each digit to a byte, simplifying display at the cost of using more storage. On machines with generous memory like IBM mainframes, unpacked BCD enabled error-checking via character operations and supported human-friendly number formatting. Overall, packed BCD optimized for compact encoding while unpacked prioritized readable representation.
### The Legacy of BCD in Numeric Computing  
Though later superseded by standardized binary encodings, BCD played an integral role in the development of computer number handling. It delivered a workable solution to represent cardinal values on nascent systems. BCD's digit-oriented design informed character-based number formats still used today. Itspacked variant influenced compact encodings forquantized data. The challenges of BCD also motivated research in binary floating point. Even as hardware outgrew BCD's compromises, it served as a bridge advancing numeric computing until true arbitrary precision binary storage emerged. BCD established foundations that enabled modern number processing.
![Understanding Binary Coded Decimal (BCD)](http://ecomputernotes.com/images/thumb587-BCD-Codes-8a4868af3bd5bd92c448b0ff26d4ae08.jpg)