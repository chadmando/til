# Get Windows OS Name and Version from CMD

Use this to find the name and version of the operating system at a Command Prompt (CMD).

```batchfile
systeminfo | findstr /B /C:"OS Name" /C:"OS Version"
```

If you are using PowerShell, pipe systeminfo to `Select-String` and look for the details.

```powershell
systeminfo | Select-String @("OS Name","^OS Version")
```

The `^` is needed to avoid grabbing the BI_OS Version_ too.


## References
The command prompt version found in the [Blue Team Field Manual]() by Alan White and Ben Clark.