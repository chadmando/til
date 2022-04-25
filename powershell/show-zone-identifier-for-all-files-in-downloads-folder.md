# Show Zone Identifier Data For All Files In Downloads Folder

Use the `-Stream` parameter to access the _Alternate Data Streams_ (ADS) in Windows files.

```powershell
Set-Location $env:USERPROFILE\downloads |
Get-ChildItem . |
ForEach-Object -Process {Get-Item $_  -Stream * -ErrorAction Ignore} |
Where-Object {$_.Stream -eq "Zone.Identifier"} |
ForEach-Object -Process {Get-Content ($_.PSPath)} |
Out-Host -Paging
```

## Stream Parameter

ADS is a Windows file feature.
The `Stream` parameter can be used with most of the `Item` and `Content` noun based cmdlets.
You can add alternate data streams using the `Add-Content` or `Set-Content` cmdlets.

## Mark of the Web

Windows tags the files which were downloaded from the internet with the _Zone.Identifier_ stream.
The stream contains a small amount of data including:

+ ZoneId 
+ ReferrerUrl
+ HostUrl

