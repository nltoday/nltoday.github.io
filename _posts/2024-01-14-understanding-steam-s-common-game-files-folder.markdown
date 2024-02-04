---
layout: post
title: "Understanding Steam's 'Common' Game Files Folder"
date: 2024-01-14 21:00:52 +0000
categories: "Gaming"
excerpt_image: https://static.savelocation.net/strapi/image_5f50821f54.png
image: https://static.savelocation.net/strapi/image_5f50821f54.png
---

### What is the 'Common' Folder Used For?
The 'Common' folder located within Steam's default installation directory is used to store game files that are shared across multiple games on your system. Steam utilizes this folder to prevent duplicating common files that are used by many different titles. Things like common engine components, texture packs, sound files and more can all be found here rather than having separate copies for each individual game folder. This helps save precious disk space.

![](https://techcult.com/wp-content/uploads/2021/10/double-click-on-steamapps-folder.png)
### [Sharing Frequently Used Game Assets](https://store.fi.io.vn/call-your-mom-mothers-gift-i-love-my-mother-your-mom-is-calling-2986) 
Rather than storing duplicate copies of frequently used game assets like textures, models or audio files separately for every installed title, Steam places shared resources in the 'Common' folder to be accessed by all applicable games. Things like common character models, landscapes, weapons and effects can live in one place rather than being copied repeatedly. This serves two main purposes - it conserves disk space which can be allocated to other uses, and it ensures game files are always in sync between titles that utilize shared content.
### Optimizing Storage Through File Deduplication
A key technique employed by Steam is **file deduplication**, which detects identical files across different game installations and avoids duplicating the data. Identical copies of common files are simply referenced from the central 'Common' folder location rather than being needlessly copied multiple times over. This allows Steam to optimize storage utilization of your drive(s) by avoiding wasteful duplication. The 'Common' folder centralizes shared assets to be efficiently accessed by all applicable games.
### How Installing Additional Games Impacts the 'Common' Folder 
As you install more and more games through your Steam library, the 'Common' folder will slowly accumulate additional shared files leveraged by the various titles. For example, installing a few more games from the same publisher or using the same game engine may deposit some common engine components or asset packs into the folder. Periodically, Steam may also deposit new shared files into 'Common' such as core system updates applied across all games. Over time, the folder size will gradually increase proportionate to your overall library as more shared references are established.
### **Managing Space Usage Through Folder Configuration**
If disk space becomes constrained, Steam provides options to configure additional **library folders** which can help spread content across multiple drives. You can choose to install certain games onto another hard drive or SSD while still allowing them to utilize shared files stored in the primary 'Common' folder location. This lets you better segment your library for storage optimization based on each game's size and access needs. You can also configure maximum cache sizes per library to auto-delete temporary files and reclaim space.
### How Game Files are Referenced from the 'Common' Folder
When you install or play a Steam game, it will access shared assets from the 'Common' folder based on reference properties stored within its own directory structure. There are symbolic links, junctions and hard links created to files in 'Common' rather than separate copies being made. The game checks its own folders first, and if a requested file isn't found locally, it will then look to 'Common' to fulfill the request instead of resulting in a missing file error. This transparently allows all installed games to leverage shared resources centralized in one optimized location.
### Resolving issues Through Verification and Reconfiguration  
In rare cases, linkage issues between games and common files can occur if files are moved or modified outside of Steam. You can right-click a game and choose "Properties" then "Local Files" tab to **verify integrity of game files** which will check and re-link any missed dependencies. The 'Common' folder can also be completely deleted and recreated by Steam if problems persist. Be sure not to manually alter or remove files within it yourself unless you understood the impact. Let Steam handle synchronization of this centralized shared content location.
### Summarizing the Purpose of the 'Common' Folder
In summary, the 'Common' folder contained within your Steam installation is used to house any game files, components or assets that are commonly referenced by multiple installed titles to avoid wasteful duplication. This centralized approach optimizes storage usage of your drives by employing techniques like file deduplication and soft linkage between games and shared resources. Over time, it will accumulate additional resources leveraged by your growing library for hugely improved efficiency versus storing everything completely separately.
![Understanding Steam's 'Common' Game Files Folder](https://static.savelocation.net/strapi/image_5f50821f54.png)