---
layout: post
title: "Understanding How Game Data is Loaded and Managed in RAM"
date: 2024-03-04 11:30:28 +0000
categories: "Gaming"
excerpt_image: http://teachcomputerscience.com/wp-content/uploads/2016/12/cache_animation.gif
image: http://teachcomputerscience.com/wp-content/uploads/2016/12/cache_animation.gif
---

## Memory Management is Key
Modern games ship with massive install sizes, sometimes exceeding 100GB, yet only require a fraction of that memory (RAM) to run smoothly. This is because of effective memory management techniques used by applications and operating systems. 
### Texture Streaming
Games only load the [texture assets](https://store.fi.io.vn/funny-chihuahuas-easter-day-bunny-eggs-easter-costume-womens-chihuahua-dog) needed for the current area into memory. As players explore new environments, unused textures are flushed out and replaced. This **streaming** process occurs seamlessly in the background.

![](https://www.learncomputerscienceonline.com/wp-content/uploads/2019/06/OS-Memory-Management-Virtual-Memory.jpg)
### Deferred Loading 
Game code, like character models, animations and scripting, is also loaded dynamically. The **core executables** are installed upfront but additional components are only brought into memory when needed. This technique, called **deferred loading**, reduces initial memory usage.
## Virtual Memory Swapping 
To accommodate apps that exceed physical RAM, operating systems employ **virtual memory** via **page swapping**. Infrequently used memory pages are written to disk, freeing space. When an application accesses a swapped page, it is automatically reloaded without the user noticing. This illusion of expanded memory is achieved seamlessly.
### Level of Detail 
Far away in-game objects have **lower resolution textures** and fewer polygons applied using **level of detail** (LOD) modeling. As the player approaches, more detailed models seamlessly replace simpler ones, optimizing graphics memory usage.
## Caching Improves Performance 
With streaming, deferred loading and LOD, often-accessed assets remain cached in RAM. The next time they are needed, they can be served directly from memory instead of being reloaded from disk. This **in-memory caching** greatly boosts performance by eliminating repeated read operations from storage.
### Multi-Core Optimization
Modern CPUs have multiple cores that can tackle different tasks simultaneously. Games leverage **multi-threading** to stream new assets from storage to memory in parallel with game logic and rendering, hiding load times and keeping gameplay smooth.
## System Requirements are Deceptive
While some games advertise requiring 8GB or more of RAM, in practice less will suffice thanks to clever memory management. The **core application** itself consumes only a fraction of advertised install sizes. Remaining game assets are efficiently streamed in and out of RAM on demand, creating the illusion of larger memory usage.
### Longtail Keyword: Virtual Memory Page Swapping Technique
By intelligently relocating less frequently accessed blocks, or pages, from RAM to disk storage, virtual memory tricks applications into thinking they have much more memory available than physically installed. This **virtual memory page swapping technique** is transparent to programs and users, seamlessly optimizing memory usage.
![Understanding How Game Data is Loaded and Managed in RAM](http://teachcomputerscience.com/wp-content/uploads/2016/12/cache_animation.gif)