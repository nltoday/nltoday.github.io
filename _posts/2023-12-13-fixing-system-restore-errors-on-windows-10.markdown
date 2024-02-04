---
layout: post
title: "Fixing System Restore Errors on Windows 10"
date: 2023-12-13 16:52:51 +0000
categories: "News"
excerpt_image: https://www.drivethelife.com/uploadfiles/20160520/W10-System-Restore-01.jpg
image: https://www.drivethelife.com/uploadfiles/20160520/W10-System-Restore-01.jpg
---

## The Issue
System Restore is an important feature of Windows that allows users to roll back their system to an earlier point in time if issues arise. However, some users may encounter error 0x80070091 when trying to perform a System Restore. This error can occur for various reasons, but usually indicates some underlying corruption or permission issue preventing System Restore from functioning properly.
### Causes and Troubleshooting
There are a few common causes for the 0x80070091 error when trying to perform System Restore in Windows 10:
Modified system files - optimizing software or tampering with system permissions could disrupt important Windows registry keys and files needed for System Restore.
Corrupted or missing files - essential system drivers, components or the specific restore point files themselves may be damaged or absent. 
Invalid file paths - if the specified restore point files can't be located, this error will result. File paths could be incorrect due to typos, deletions or system tampering.
Lack of permissions - user account privileges may need to be adjusted to allow accessing and restoring system files.
The first steps in troubleshooting involve basic resets and permissions checks. Restarting in Safe Mode can isolate driver or software conflicts. Verify file paths are correct and permissions allow restore access. Uninstalling recently added programs is also recommended.
If the issue persists, more comprehensive repairs may be needed. But performing a System Restore is the ideal solution if it can be made to work again. The following methods provide workarounds to common causes of the 0x80070091 error.

![](https://i.ytimg.com/vi/hxnJYJ9S3xo/maxresdefault.jpg)
## Repairing System Restore Folder Permissions
One common reason for this error involves corrupted or blocked permissions on the hidden WindowsRestore folder containing restore point files. Taking ownership and adjusting permissions can re-enable System Restore functionality.
### Adjusting Folder Ownership 
1. Press Windows key + X and select Command Prompt (Admin)
2. Type "takeown /f %windir%\System32\config /r /d y" and press Enter
3. Type "icacls %windir%\System32\config /grant administrators:F" and press Enter 
### Adjusting Folder Permissions
1. Type "attrib %windir%\System32\config\systemprofile\appdatalow -h -s" and press Enter
2. Type "icacls %windir%\System32\config\systemprofile\appdatalow /grant administrators:F" and press Enter
## Using DISM and SFC Scans for Comprehensive Repairs
If folder permissions or other basic fixes don't resolve the issue, the system likely needs more thorough repairs. Windows Deployment Image Servicing and Management (DISM) and System File Checker (SFC) scans can repair corrupted system files allowing System Restore to function again.
### Running DISM and SFC Scans
1. Open an Admin Command Prompt 
2. Type "Dism /Online /Clean-Image /RestoreHealth" and press Enter
3. Type "sfc /scannow" and press Enter
4. Restart and retry System Restore
The DISM tool repairs issues with Windows image files while SFC replaces any corrupted important system files. This can fix various underlying causes preventing System Restore from working properly.
## Backing up Your System State
If all else fails and System Restore remains unusable, your only option left may involve resetting or reinstalling Windows. But first it's important to back up your system state to prevent data loss. 
### Creating a System State Backup
1. Open Control Panel > System and Security > Backup and Restore
2. Click "Create a system image" and follow the prompts
3. Save the backup file to an external drive for safety
With a recent system image backup in place, you can safely reset or reinstall Windows knowing all personal files and settings will be preserved. Just restore the backup after to get your system functionality back without losing personal data. This provides a workaround even if System Restore itself can no longer be relied on.
## Resetting or Reinstalling Windows as a Last Resort
If fundamental system corruption prevents any restoration methods from working, a complete reset may be needed. The two main options are resetting Windows without losing files, or a clean reinstallation.
### Resetting Windows via Settings App
1. Open Settings > Update & Security > Recovery
2. Click "Get started" under "Reset this PC" 
3. Choose to keep files or fully clean install Windows
### Performing a Clean Reinstall of Windows  
1. Create Windows installation media using the Media Creation Tool
2. Boot from the media and select "Install now"  
3. Choose to perform a clean install and follow prompts 
While resetting or reinstalling should resolve the deepest system issues, it's a last resort after other methods fail. A recent system backup allows restoring user files and settings easily afterward.
## Summary
The 0x80070091 error when performing System Restore indicates an underlying issue that needs addressing. Basic troubleshooting steps like restarting in Safe Mode, verifying file paths and permissions are the first approach. For more thorough repairs, DISM and SFC scans can fix corrupted system files enabling restore functionality. As a last option, resetting or reinstalling Windows resolves even fundamental system corruption if needed. With careful documentation and backups, these methods provide effective solutions for fixing System Restore problems on Windows 10.
![Fixing System Restore Errors on Windows 10](https://www.drivethelife.com/uploadfiles/20160520/W10-System-Restore-01.jpg)