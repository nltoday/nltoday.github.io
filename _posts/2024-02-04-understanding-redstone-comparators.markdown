---
layout: post
title: "Understanding Redstone Comparators"
date: 2024-02-04 05:24:15 +0000
categories: "News"
excerpt_image: https://i.ytimg.com/vi/pUkkNfXU5YA/maxresdefault.jpg
image: https://i.ytimg.com/vi/pUkkNfXU5YA/maxresdefault.jpg
---

Redstone comparators are redstone components in Minecraft that can compare signal strengths and output redstone signals based on the comparison. They have versatile uses from item sorting systems to automatic farming setups. Let's take a deeper look at how comparators work and different ways we can utilize them.
### Comparing Signal Strengths
A comparator requires two redstone inputs - one at the back and one at the side. It will compare the strength of the redstone signal entering from each side. The signal strength is determined by the type of block emitting the signal. For example, a torch emits a strength of 1 while redstone dust at its maximum emits a strength of 15. 
If the back signal is stronger, the comparator will output a signal in [subtract mode](https://store.fi.io.vn/collection/akridge). In compare mode, it will output a signal only if the back signal is weaker than the side signal. Understanding these comparison modes is key to using comparators effectively.

![](https://i.ytimg.com/vi/T95-6dln4Eg/maxresdefault.jpg)
### Subtract Mode in Action 
In subtract mode, the comparator subtracts the back signal strength from the side signal strength and uses the result as its output strength. If the back is stronger, it cannot output a negative number so there is no output signal. 
For example, if the side signal is strength 5 and back is strength 3, it will output a strength of 5 - 3 = 2. But if the back is strength 7, being stronger, it will output nothing. This subtract mode is useful when you want the output to decrease as an input increases.
### Compare Mode Functionality
Compare mode activates an output signal only when the back signal is weaker than the side signal. In my previous example, if in compare mode, it would output a signal only when the back strength is 3 since that is weaker than the side strength of 5. 
But if the back was strength 7, being stronger, it would not output any signal. Compare mode is great for triggering events based on signal strength comparisons like item sorting.
### Practical Item Sorting System
One popular use of comparators is building automatic item sorting systems. We can leverage both subtract and compare modes. Items enter a chest connected to the side of a comparator. 
Empty chests will output the maximum signal strength. As items fill the chest, its signal strength reduces. When it drops below the back signal strength set by redstone dust or other blocks, the comparator will output a signal triggering a sorter mechanism.
By using multiple chests each with their own comparator and adjusting the back signals accordingly, we can sort stacks of items into their designated storage chests based on signal drop-off points. This allows fully automatic **item sorting systems** without much redstone logic.
### Other Practical Uses of Comparators
Another common use of comparators is reading the number of items or amplification levels in containers like note blocks, **jukeboxes**, brewing stands etc. 
For example, connecting a comparator to a note block playing a specific note allows reading the playback progress as a output signal. This finds uses in musical contraptions. 
Comparators are also useful in smart farms that can detect crop growth, number of mobs in an area or minecart loading/unloading through signal strength comparisons and outputs. 
Overall comparators provide a versatile tool for reading block states and making output decisions based on signal readings, powering numerous automation contraptions in Minecraft.
### Comparator Input and Output Signals  
To summarize the key aspects, a comparator has a back input and a side input. In subtract mode, it outputs the difference between the two signal strengths. In compare mode, it activates output only if the back is weaker than the side.
The output can further be strengthened by placing redstone dust/repeater behind the comparator. Its versatility in reading container block states and outputting logic makes it indispensable for **redstone circuitry** and complex automation systems. Proper usage of subtract and compare modes is important to leverage its full potential.
### Comparator Quirks and Technical Details
While comparators function based on signal strength comparisons, there are some technical quirks to be aware of. Chests can only output a maximum strength of 11 regardless of fill. 
Hoppers behave differently depending on which side items are inserted - the bottom can output 15. Comparators also output a low signal of 1 even when there is no input. 
These technical behaviors require compensating the redstone logic when building complex circuits. Overall, with practice and understanding of these quirks, comparators become quite straightforward to utilize in diverse situations.
### In Summary
In this guide, we took an in-depth look at how redstone comparators work and their key functionalities - subtract and compare modes, practical uses like item sorting and output reading, technical behaviors and input-output signals. 
Comparators are a versatile and fundamental component that helps bring automation and logic to many complex contraptions in Minecraft from automatic farms to advanced circuits. With practice applying the concepts covered here, you can efficiently leverage comparators for your creations.
![Understanding Redstone Comparators](https://i.ytimg.com/vi/pUkkNfXU5YA/maxresdefault.jpg)