# Measure the Execution Time of a Command or Function

To determine how long it take to execute a command, use the `Measure-Command` cmdlet.
`Measure-Command` returns a `System.Timespan` object.

## Example

```powershell
Measure-Command {Get-Process; Get-Service}
```

Results will look like:

```text
Days              : 0
Hours             : 0
Minutes           : 0
Seconds           : 0
Milliseconds      : 557
Ticks             : 5579940
TotalDays         : 6.45826388888889E-06
TotalHours        : 0.000154998333333333
TotalMinutes      : 0.0092999
TotalSeconds      : 0.557994
TotalMilliseconds : 557.994
```

## References

Check the help for command options and examples, `Get-Help Measure-Command -Full`.