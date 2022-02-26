# Get the Full Path of a Shorted PSDrive

Use the `Convert-Path` cmdlet to find the full path of a shortened `PSDrive`.

If you have a shortened drive.

```powershell
New-PSDrive -Name mydocs -PSProvider FileSystem -Root /Users/chadmando/Documents/
```

While using the PSDrive, you can get the full Root path using `Convert-Path`.

```powershell
PS mydocs:/>Convert-Path $PWD
/Users/chadmando/Documents/
```

More on the `Convert-Path` can be found in the [Microsoft Docs](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/convert-path?view=powershell-7.2)
