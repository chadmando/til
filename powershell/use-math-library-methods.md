# Use Math Library Methods

Use the `[Math]` .NET Class to access more mathematical methods and constants.

## Methods

To find the absolute value of a number:

```powershell
[Math]::Abs(-8)
```

See all of the available methods and constants by piping to `Get-Member`.

```powershell
[Math] | Get-Member -Static -MemberType All
```

## References

+ A more detail write-up of available functions by  4sysops is [here](https://4sysops.com/archives/do-the-math-with-powershell/).
+ Math Class [documentation](https://docs.microsoft.com/en-us/dotnet/api/system.math?view=net-6.0) 