# Get Windows OS Name and Version from CMD

Use this to find the name and version of the operating system at a Command Prompt (CMD).

```batchfile
systeminfo | findstr /B /C:"OS Name" /C:"OS Version"
```

If you are using PowerShell, pipe systeminfo to `Select-String` and look for the details.

```powershell
systeminfo | Select-String @("OS Name","^OS Version")
```

The `^` is needed to avoid grabbing the BIOS Version too.


## References
The command prompt version found in the [Blue Team Field Manual](https://www.amazon.com/Blue-Team-Field-Manual-BTFM/dp/154101636X) by Alan White and Ben Clark.
