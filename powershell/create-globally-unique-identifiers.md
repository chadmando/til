# Create A Globally Unique Identifier (GUID)

PowerShell has a cmdlet for generating GUIDs. 

```powershell
New-Guid
```

Result:

```text
Guid
----
895dc56b-6542-4029-a5de-6502743aa136
```

Of course, each result is _unique_.
Results can use used in a script or saved to a variable.
This is an simple way to generate the key field for a database.

## References

Overall this cmdlet is simple and the best reference is the [Microsoft docs](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/new-guid?view=powershell-7.2).
