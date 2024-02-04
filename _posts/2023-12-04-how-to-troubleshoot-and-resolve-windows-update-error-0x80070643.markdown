---
layout: post
title: "How to Troubleshoot and Resolve Windows Update Error 0x80070643"
date: 2023-12-04 22:33:32 +0000
categories: "Tech"
excerpt_image: https://www.minitool.com/images/uploads/articles/2021/04/fix-windows-update-error-0x80070643/fix-windows-update-error-0x80070643-1.png
image: https://www.minitool.com/images/uploads/articles/2021/04/fix-windows-update-error-0x80070643/fix-windows-update-error-0x80070643-1.png
---

Windows Update errors can be frustrating to deal with, but with the right troubleshooting steps, the solution is usually within reach. This comprehensive guide will walk you through various methods to identify and fix error code 0x80070643. Let's get started.
### Clear the Update Cache  
The Windows Update cache stores temporary files related to updates and can become corrupted over time. Clearing this cache is one of the simplest things to try first. Open an administrator command prompt and run the following commands to delete and recreate the necessary folders:
```
net stop wuauserv  
net stop cryptSvc
net stop bits
net stop msiserver
ren C:\Windows\SoftwareDistribution SoftwareDistribution.old
ren C:\Windows\System32\catroot2 catroot2.old
net start wuauserv
net start cryptSvc 
net start bits
net start msiserver
```

![](https://images.drivereasy.com/wp-content/uploads/2017/09/img_59a8d22a9b2e7.jpg)
### Run the Windows Update Troubleshooter
The Windows Update troubleshooter is designed to automatically detect and fix common update issues. Open Settings, go to Update & Security, and select Troubleshoot on the left. Click "Windows Update" and let the troubleshooter do its thing. It may find and resolve the underlying cause of error 0x80070643.
### Restart Your Computer
Sometimes a simple reboot is all that's needed to resolve Windows Update errors. Ensure all programs are closed and give your PC a fresh start. Then try installing updates again once the computer has fully restarted.
### Check For Enough Disk Space
Insufficient free space on your hard drive can prevent updates from downloading or installing properly. Make sure to have at least 20GB of available disk space before attempting updates. Free up space by deleting unnecessary files if needed.
### Disable Antivirus and Firewall Temporarily  
antivirus software or firewall settings may be interfering with the [Windows update process](https://store.fi.io.vn/womens-crazy-beagle-lady-dog-lover-v-neck-t-shirt/men&). Temporarily disabling these programs lets Windows Update run uninterrupted to see if that's the root cause. Be sure to re-enable security features once troubleshooting is complete.
### Manually Install Failed Updates
If a specific update is consistently failing to install, you can download its individual file from the Microsoft Update Catalog and manually run the installation through Control Panel or Powershell. Manually overriding the built-in updater avoids troublesome spots.
### Check for System File Corruption
Operating system files getting corrupted over time can introduce strange issues like 0x80070643. Run the system file checker (SFC) and Deployment Image Servicing and Management (DISM) tools from an elevated command prompt to check and repair file integrity:
```
sfc /scannow
dism /online /cleanup-image /restorehealth
```
These utilities will detect and correct any broken system files that may be blocking updates.
### Update Graphics and Network Drivers
Outdated drivers, especially for graphics cards or network adapters, have been known to conflict with Windows Update functionality. Check for and install the latest versions distributed by the **driver manufacturers** to rule out incompatible software as the cause.
At this point, most common 0x80070643 errors should be resolved. But if still no luck, further possibilities like file permission issues or hard drive faults may need attention from the Microsoft support team. With thorough troubleshooting, the solution is achievable.
### Perform a Repair Installation
For severe update failures, a repair or "in-place" installation of Windows 10 that preserves user files and settings could help reset the operating system to a known healthy state. Use the Media Creation Tool to create install media, then choose the "Keep personal files and apps" option during setup. This refreshes Windows without a full reinstallation. As a last resort, it may solve whatever underlying corruption was blocking updates.
Update issues are frustrating but often have straightforward fixes. With methodical testing of solutions like those outlined here, error 0x80070643 should be resolved without much difficulty. Feel free to consult Microsoft documentation or support as needed for any additional troubleshooting guidance specific to your situation.
![How to Troubleshoot and Resolve Windows Update Error 0x80070643](https://www.minitool.com/images/uploads/articles/2021/04/fix-windows-update-error-0x80070643/fix-windows-update-error-0x80070643-1.png)