---
layout: post
title: "Fix the error 0x8007000D when trying to activate Windows"
date: 2024-01-20 19:58:27 +0000
categories: "Tech"
excerpt_image: https://ugetfix.com/wp-content/uploads/articles/askit/how-to-fix-error-code-0x8007000d-on-windows_en.jpg
image: https://ugetfix.com/wp-content/uploads/articles/askit/how-to-fix-error-code-0x8007000d-on-windows_en.jpg
---

### Causes and troubleshooting steps
This common error typically arises when trying to activate Windows using a product key. The system account has default full control permissions over the registry path HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\Root and its subkeys. If those permissions have been altered, it can cause the 0x8007000D error.
Some troubleshooting steps to resolve it include:
1. Check permissions and assign minimum rights
- Check the permissions on the registry path and subkeys
- Assign the minimum "Enumerate Subkeys" permission to the System account
2. Run the Fix it wizard 
- Microsoft provides a Fix it wizard to automatically assign the required permissions
- Download and run the wizard to follow the steps
3. Perform a Windows update
- Outdated Windows installations can cause activation issues
- Ensure Windows is fully updated to the latest version
4. Clear temporary files and cleanup
- Temporary files can sometimes interfere with the activation process
- Use CCleaner to clear cache, temporary files and optimize the registry
5. Create a new user account
- As a last resort, create a new user account to test if it's account specific
- Backup important files before deleting the problem account
6. Check network and security software
- Firewalls, antivirus or other security programs could potentially block activation
- Temporarily disable them to test if they are interfering 
7. Try contacting support for further assistance
- If the issue persists even after troubleshooting, seek support
- Provide logs and error details for deeper troubleshooting

![](https://techcult.com/wp-content/uploads/2017/06/Fix-Error-Code-0x8007000D-when-trying-to-activate-Windows.png)
### Assigning registry permissions 
To assign the required permissions manually:
1. Open the Run dialog and type `regedit` to launch the Registry Editor
2. Navigate to `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\Root` 
3. Right click the Root key, select [Permissions](https://store.fi.io.vn/chihuahuas-blue-chihuahua-dog-weightlifting-in-fitness-gym-chihuahua-dog) then click **Add** 
4. Select **SYSTEM** from the list of entries and check **Enumerate subkeys**
5. Click **OK** and repeat the process for any other subkeys showing permission errors
6. Try activating Windows again after assigning the minimum rights
### Using the Microsoft Fix it utility
For an automated solution, download and run the Fix it tool:
1. Go to [fix the error link](http://go.microsoft.com/?linkid=9741048)
2. Click **"Fix this problem"** then **"Run"** to start the wizard 
3. Follow the on-screen steps to allow the tool to assign the required registry permissions
4. No need to manually edit registry - the utility handles it automatically
5. Reboot if asked and try activating Windows once more
In most cases, using the Fix it tool or manually assigning the minimum permissions is sufficient to resolve the 0x8007000D activation error. It addresses the underlying cause by correcting any altered registry authorizations.
![Fix the error 0x8007000D when trying to activate Windows](https://ugetfix.com/wp-content/uploads/articles/askit/how-to-fix-error-code-0x8007000d-on-windows_en.jpg)