# Fix User Profile Using Registry Edits

## Assumptions

+ Windows 11 Pro - Microsoft Intune Managed
+ User is a Microsoft Work account (i.e. EntraID)

## Problem

When a Windows User's profile has a problem, Windows may allow them to log in and point their profile to a temporary location, `C:\Users\TEMP` instead of `C:\Users\<UserName>`.
The users will complain that all items have *disappeared* from the Desktop or that applications are missing.

## Solution

After posting a questions on the Microsoft Tech Community site[^1], I received these instructions from a community member. I have made some cosmetic edits for readability.

1. Open the Registry Editor:

1. Go to the path: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\ProfileList`. Within ProfileList, you will see several subkeys with names in SID (Security Identifiers) format. Each SID corresponds to a user account on the computer.

1. Click on each SID and look for the ProfileImagePath entry in the right-hand pane. This entry shows the path to the user's profile (for example, C:\Users\name.surname).

1. Identify the SID associated with the problem user profile by verifying that the ProfileImagePath is correct (i.e., C:\Users\name.surname).

### If You See A .bak Suffix

You may notice two identical SID entries, one of which ends in .bak. This usually indicates that the profile has been flagged as problematic.

1. Rename the current SID (the one without .bak) by adding `.old` to the end.

1. Remove the .bak suffix from the other SID entry (the one with the original profile path).

### If There Is No .bak Suffix

If the correct SID has a ProfileImagePath pointing to C:\Users\TEMP:

1. Change the path and put it back to the original one (i.e., C:\Users\name.surname>).

1. Reboot and verify

## References

[^1]: My question on the [Microsoft Tech Community](https://techcommunity.microsoft.com/t5/microsoft-entra/entraid-account-on-windows-11-being-started-under-a-temp-user/m-p/4281720#M9937)
