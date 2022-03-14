# Encode Binary File as a Base64 String

Use the `[System.Convert]` .NET Class to convert an array of Byte objects to a Base64 string.


Get bytes into a variable using the `Get-Content` cmdlet.

```powershell
$arrayOfBytes = Get-Content c:\path\to\binary\file.bin -Encoding Byte -Raw
```

Use the _ToBase64String_ method to convert to the Base64 string.

```powershell
$base64string = [System.Convert]::ToBase64String($arrayOfBytes)
```

To get back to a binary file, use the _FromBase64String_ method.

```powershell
[System.Convert]::FromBase64String($base64string) | 
Set-Content -Path c:\new\path\to\binary\file.bin -Encoding Byte
```

## References

+ [Convert](https://docs.microsoft.com/en-us/dotnet/api/system.convert?view=net-6.0) documentation
+ For more on `Get-Content` and `Set-Content` reference help in PowerShell. e.g. `Get-Help Get-Content -Full`
