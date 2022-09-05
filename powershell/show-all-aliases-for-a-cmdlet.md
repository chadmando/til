# Show All Aliases For A Cmdlet

PowerShell contains many standard aliases for cmdlets.
To see the aliases for a cmdlet use `Get-Alias` with the `-Definition` parameter.

## Example

You want to find all the aliases for the `Remove-Item` cmdlet.

```powershell
Get-Alias -Definition Remove-Item | Select-Object -Property Name
````

Results

```text
Name
----
del
erase
rd
ri
```
