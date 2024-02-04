---
layout: post
title: "Fixing the Access Denied Error 0x80070005"
date: 2023-12-14 20:55:45 +0000
categories: "Tech"
excerpt_image: https://images.drivereasy.com/wp-content/uploads/2016/07/img_57919cb1630b8.png
image: https://images.drivereasy.com/wp-content/uploads/2016/07/img_57919cb1630b8.png
---

Windows Access Denied Error 0x80070005 is a frustrating error that prevents users from accessing files, folders, and drives on their systems. This error occurs when the user does not have adequate permissions to access the resource they are trying to open. There are a few straightforward solutions that can help resolve this issue and regain access.
### Giving Yourself Full Administrator Permissions
One common cause of the access denied error is that the user account does not have administrator-level permissions. [administrator permissions access error](https://store.fi.io.vn/work-hard-so-my-st-bernard-live-a-better-dog-lover-2) can be easily fixed by taking ownership of the files or folders and granting full control permissions. Follow these steps:
1. Open the C:\Users\USERNAME\AppData folder through Windows Run dialog. 
2. Right-click on AppData, open Properties, go to Security tab, and click Edit.  
3. Click Add and add the username, check names, and hit OK.
4. Select the username, set permissions to Full Control, and click OK.
5. Reboot for changes to take effect.

![](https://www.geekdashboard.com/wp-content/uploads/2017/07/Error-0x80070005-Access-is-Denied.jpg)
### Performing a Clean Boot
Sometimes incompatible or corrupted applications and services can cause access issues. Performing a clean boot strips down startup programs to basic drivers and services. This helps isolate issues causing the error. 
1. Open msconfig through Start Search.  
2. Go to Services tab, select Hide all Microsoft services and click Disable all.
3. Go to Startup tab and open Task Manager to disable problematic programs.
4. Click OK and restart in clean boot mode.
### Checking and Repairing Drive Permissions
Corrupted or incorrect drive permissions are another common cause. Use the steps below to check and repair permissions.  
1. Right-click drive in Explorer, select Properties > Security > Advanced.  
2. Click Change owner, add username, and confirm.  
3. Right-click drive, select Properties > Security > Edit > Full Control.
4. Use CHKDSK to scan and repair hard drive errors in Command Prompt.
### Identifying and Removing Malware Infections
Malware can interfere with user account privileges and permissions resulting in access denied errors. It is important to scan and remove infections using reliable antivirus software.
1. Run a full system scan with antivirus and remove any detected threats.    
2. Use anti-malware tools like Malwarebytes to thoroughly scan for rootkits and Advanced Persistent Threats (APTs).
3. Remove cookies, cache and temporary files which can harbor malware.
4. Update Windows and install all important security patches.
### Troubleshooting Technical Issues on Virtual Private Networks 
If the access denied error occurs on files that require a VPN connection, there may be technical issues preventing the required secure connection. 
1. Check VPN service/firewall logs for errors providing clues to connectivity issues.
2. Verify authentication credentials and VPN protocols and settings are correctly configured.  
3. Use a different VPN client software if issues persist with current client.
4. Contact VPN provider for assistance if problems remain unresolved.
### Restarting in Safe Mode  
As a last troubleshooting step, boot into Windows Safe Mode which loads only essential drivers and services. This rules out software compatibility issues causing access denied problems.
1. Restart computer and repeatedly tap F8 key on startup to access Advanced Boot Options.  
2. Select Safe Mode from menu and log in with administrator credentials.
3. Attempt accessing files and check if error recurs, then restart as usual.
By methodically testing each solution, the root cause of the access denied error can be pinpointed and addressed to regain control and usability of affected systems and files. Regular reviews of user permissions and vigilance against malware also help prevent recurrence of this frustrating Windows problem.
![Fixing the Access Denied Error 0x80070005](https://images.drivereasy.com/wp-content/uploads/2016/07/img_57919cb1630b8.png)