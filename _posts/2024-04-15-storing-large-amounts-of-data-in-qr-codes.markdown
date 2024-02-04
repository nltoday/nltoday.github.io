---
layout: post
title: "Storing Large Amounts of Data in QR Codes"
date: 2024-04-15 18:18:44 +0000
categories: "Tech"
excerpt_image: https://www.techspot.com/articles-info/1676/images/2018-08-30-image-5.png
image: https://www.techspot.com/articles-info/1676/images/2018-08-30-image-5.png
---

### QR Code Specifications and Limitations
QR codes have standard specifications that determine the maximum amount of data that can be encoded based on the data type. The most common data types are [numeric only](https://store.fi.io.vn/collection/corgi), **alphanumeric**, **binary/byte**, and **Kanji/Kana characters**. According to Wikipedia, the specifications for each data type in a standard or static QR code are as follows:
- **Numeric only:** Up to 7,089 characters consisting of digits 0 to 9.  
- **Alphanumeric:** Up to 4,296 characters consisting of digits 0 to 9, uppercase letters A to Z, space, and common symbols like $, %, *, +, -, etc.
- **Binary/byte:** Up to 2,953 bytes or 23,624 bits that can represent text encoded in ISO/IEC 8859-1.
- **Kanji/Kana:** Up to 1,817 characters of Japanese script encoded in Shift JIS X 0208 standard.
So in summary, the maximum amount of data that can be stored in a standard QR code ranges from under 8,000 characters for numeric only data down to under 2,000 characters for Kanji text. This poses limitations if you need to encode a large amount of **more than 20,000 characters** of text or other data into a single QR code.

![](https://f5s3r6h9.rocketcdn.me/wp-content/uploads/2020/07/qr-code-structure.png)
### Using Multiple QR Codes or Dynamic QR Codes 
One way to store data exceeding the limits of a single standard QR code is to split it across multiple QR codes. However, this is not very user-friendly as the end-user would need to scan multiple codes to access all the data. 
A better approach is to use a **dynamic QR code** which allows encoding significantly more data compared to standard QR codes. Dynamic QR codes can encode thousands of words of text, PDF files, documents etc. by linking to an online resource. So it is possible to encode over 20,000 characters of text into a single dynamic QR code.
### Compressing and Encoding Large Files
For certain types of large files like text documents, it may be possible to compress and encode the file itself within the payload capacity of a standard QR code. One method demonstrated on mattkc's YouTube channel is:
1. Take the text file containing 20,000+ characters  
2. Compress it using zip or similar archive utility
3. If the compressed file size reduces below the 7KB payload limit of QR code version 40, then it can be directly encoded.
However, high compression ratios could potentially corrupt the data. So proper testing is required to optimize the compression without losing integrity of encoded information.
### Storing a Game within a QR Code
In an interesting proof-of-concept, mattkc demonstrated storing an entire playable **Snake game** within a single standard QR code. The game application was first minimized using Crinkler tool to reduce its size from original 3.2KB to around 1.4KB. 
Then the minimized executable was directly encoded into the QR code. By scanning the code using a webcam-based reader like zBar, the end-user was able to launch and play the whole Snake game extracted from the QR code payload. This showcased the potential of standard QR codes for encoding small interactive programs and applications.
### Accessing Large Amounts of Data 
While it may not be feasible to directly encode tens of thousands of characters into a standard QR code, the QR code payload can still be effectively used to access large datasets. The ISO QR code specification details provide the payload link as follows: 
"As far as "more space", you should think of the QR code as a "link", or a "shortcut" to your URL. Clicking the QR code b rings the user to web site; once they're there, you have as much space as you want."
So a QR code can simply contain a URL link to an online file, document, webpage etc. hosting the large amount of data. This allows unlimited data capacity while maintaining the convenience of accessing it via a QR scan.
### Putting It All Together
In summary, while standard QR codes have limitations of under 8,000 characters of maximum payload size, there are practical techniques to encode and access much larger datasets:
- Use dynamic QR codes linking to online resources 
- Compress and encode large files within QR code capacity
- Split content across multiple QR codes
- Use QR codes as "links" to external webpages hosting unlimited data
Proper optimization of compression, file formats and linkage approaches can enable encoding tens of thousands of characters or entire interactive programs within QR codes. Overall they provide a very convenient interface for mobile access of large online datasets.
### Future Possibilities
As QR code specifications continue evolving to support more advanced data types and larger payloads, the potential uses will also increase. Already newer variants like Micro QR codes and cQR codes have emerged offering higher densities. 
Interesting future possibilities include:
- Integrating QR codes directly into product packaging and labels for multimedia product catalogs  
- Encoding 3D models, animations and even small apps/games within QR codes
- Linking physical objects and environments to virtual/augmented reality experiences
- Dynamic QR codes updating content based on location, time or user
With ongoing innovation, QR codes promise to grow into a ubiquitous interface between physical and digital worlds for accessing large datasets on mobile devices. Their impact could extend across many sectors in the coming years.
![Storing Large Amounts of Data in QR Codes](https://www.techspot.com/articles-info/1676/images/2018-08-30-image-5.png)