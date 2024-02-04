---
layout: post
title: "How to Quickly Check if a String Contains Only Numbers in Specific Positions"
date: 2023-12-08 05:00:15 +0000
categories: "Writing"
excerpt_image: https://i.ytimg.com/vi/UR3Esn7_lsE/maxresdefault.jpg
image: https://i.ytimg.com/vi/UR3Esn7_lsE/maxresdefault.jpg
---

Understanding basic programming concepts like verifying string inputs is an important foundation. In this article, we will discuss how to quickly check if a string contains only numbers in specific positions using bitwise operations.
### Leveraging Bitwise Operations
When validating strings with a limited set of possible values, bitwise operations can provide an extremely efficient solution. The core idea is to store the presence of each value in a bitmask, allowing instantaneous checking without searching arrays.
For our example of validating numbers in odd positions, we can store the numbers 0-9 in a bitmask with 1 bit per value. To set a bit, we left shift 1 by the number position and bitwise-OR it with the mask. Checking if a bit is already set simply requires a bitwise AND with the input value left shifted similarly. With only 10 possible values, a 32-bit integer is perfectly sized.

![](https://i.ytimg.com/vi/_qgaFQ3Fjfg/maxresdefault.jpg)
### Building the Validation Logic
The validation logic follows these steps:
1. Initialize a 32-bit integer mask to 0 to track seen numbers  
2. Iterate through string positions 1, 3, 5, 7 etc
3. If the character is a number, left shift 1 by the number and OR it into the mask
4. Left shift the number by the same amount and AND with the mask to check duplicates
5. If no duplicate, continue, else return invalid
6. After the loop, if the mask is non-zero, the string is valid
This approach allows **constant-time** validation without any lookups - a huge performance gain over array-based solutions for small value sets.
### Applying to the Problem
To apply this to our homework example, we would:
1. Loop through positions 1,3,5,7 
2. Convert characters to integers and shift/OR into a bitmask
3. Shift/AND to check for duplicates
4. After the loop, if the mask is non-zero, the input is valid
This provides an extremely [efficient](https://store.fi.io.vn/chihuahua-sugar-skull-dog-halloween-gift4738-t-shirt) and **concise** solution to validate numbers appear only in the given positions of a string.
### Further Optimization 
Some additional optimizations are also possible. Since we know the string length, an early return can skip unnecessary iterations. We could also right-shift the duplicate check value and avoid a second shift for even faster validation. With practice, these bitwise programming techniques become second nature for optimizing similar constraints.
Overall, bitwise operations provide a clean and fast approach when membership in a small set needs validating. The core concepts illustrated here can translate to many related problems. Understanding these building blocks of programming helps create robust and optimized solutions.
![How to Quickly Check if a String Contains Only Numbers in Specific Positions](https://i.ytimg.com/vi/UR3Esn7_lsE/maxresdefault.jpg)