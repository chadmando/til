# Get Serial Number of a Computer in PowerShell

Use the `Get-CIMInstance` cmdlet and access the `Win32_Bios` class.

```powershell
Get-CIMInstance -ClassName Win32_Bios | Select-Object -Property SerialNumber
```

