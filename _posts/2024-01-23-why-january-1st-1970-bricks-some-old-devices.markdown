---
layout: post
title: "Why January 1st, 1970 Bricks Some Old Devices"
date: 2024-01-23 23:31:47 +0000
categories: "Programming"
excerpt_image: https://i.ytimg.com/vi/ofnq37dqGyY/maxresdefault.jpg
image: https://i.ytimg.com/vi/ofnq37dqGyY/maxresdefault.jpg
---

### Tracking Time on Computers
The standard method used by computers and operating systems to keep track of time is by counting the number of seconds that have passed since midnight on January 1st, 1970. This date is known as the "Unix epoch" and the system is called "Unix time". Counting seconds in this way allows computers to represent any date after January 1st, 1970. Most modern operating systems today still use this [Unix time format](https://store.fi.io.vn/collection/dog-dad) to track elapsed time internally. 

![](https://i.ytimg.com/vi/MVI87HzfskQ/maxresdefault.jpg)
### The 32-bit Limitation
Historically, operating systems have stored the Unix timestamp as a 32-bit signed integer. This format can represent numbers ranging from -2,147,483,648 to 2,147,483,647. Converting this range to dates, it allows the representation of timestamps from December 13th, 1901 to January 19th, 2038. Once the timestamp reaches the maximum value of 2,147,483,647 seconds past the epoch, an overflow occurs. 
During an overflow, the number "wraps around" and instead of increasing, it decreases to the minimum permitted value of -2,147,483,648 seconds. On modern computers this wouldn't cause many issues beyond an inaccurate system clock display. However, for older systems still actively used, it could cause failures in applications relying on accurate time values.
### Solving the 2038 Problem
Fortunately, most modern computers, operating systems, and software have moved to 64-bit integers to represent Unix timestamps. This format provides enough capacity to count seconds for billions of years into the future well beyond any conceivable need. So systems updated in the past two decades are unlikely to be affected by the upcoming 32-bit overflow in 2038.
### Legacy Systems at Risk
Some really old computer systems from the 1970s-1990s are still in active use today, particularly in industrial automation, utilities, scientific research equipment, and other specialized applications. Mainframes, microcontrollers, embedded devices running legacy real-time operating systems built during that era commonly stored timestamps as 32-bit integers. If unaddressed, these legacy systems could face failures or glitches beginning January 19th, 2038.
### Preparing for Y2K38
To ensure critical systems remain functioning decades into the future, prudent organizations have begun auditing hardware and software for **Y2K38 compliance**. Where legacy components cannot practically be replaced, workarounds are deployed like date roll-forward patches. Other solutions involve migrating applications off **32-bit** hardware to modern 64-bit servers. With proactive remediation, the impending overflow of 32-bit Unix timestamps in 2038 need not cause widespread disruptions.
### The GPS Week Number Rollover
GPS receivers also faced a similar issue in 2019 due to using a 10-bit field to count weeks since January 6th, 1980. Wrapping after 1,024 weeks, the counter would roll over, potentially causing loss of positioning data. Manufacturers addressed this by upgrading firmware in advance to avoid any impact from the **GPS time standard** transition. The lesson emphasizes the importance of planning decades ahead for embedded systems dependent on accurate timekeeping.
### 64-bit As A Long Term Solution 
While 64-bit timestamps solve the issue for the foreseeable future, no representation of time is truly perfect. **GetTickCount()**  in Windows previously suffered from overflow within 48 days due to using only 32-bit for milliseconds since boot. Upgrading to 64-bit **GetTickCount64()** avoided this problem, showing how evolving to wider data types ensures accurate time measurement for generations to come. With proactive upgrades, computing platforms can seamlessly span centuries without disruption from overflowing time values.
### Preparing Early Avoids Disruption
As with the Y2K event and earlier GPS rollover, advance notice gives organizations ample time to audit and patch mission-critical systems as needed, avoiding unwanted surprises. By raising awareness of time standard transitions like Y2K38 years ahead, upgrades can be scheduled efficiently without rushing at the last moment. With diligent preparation, future changes to Unix timestamps and other time formats need only be curious milestones, not sources of unplanned outages or downtime. Acting now ensures continuity of services for the public well into the 22nd century and beyond.
### In Summary 
While the impending 32-bit Unix timestamp overflow in 2038 may seem like a distant problem, its ramifications emphasize the importance of long term planning for accurate timekeeping across generations of hardware. By proactively addressing issues years in advance, upgrading software where possible and isolating legacy components as needed, organizations can help ensure critical systems remain fully functional decades into the future without unexpected disruptions. With ongoing preparations, we can help bridge computers of the past with those of the yet-unknown future.
![Why January 1st, 1970 Bricks Some Old Devices](https://i.ytimg.com/vi/ofnq37dqGyY/maxresdefault.jpg)