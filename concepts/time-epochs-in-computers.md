# Time Epochs In Computers

An _epoch_ is an artificial zero point in time from which the _system time_ is measured.

The most common epoch is the Unix epoch which sets the zero point at midnight (UTC) January 1, 1970.
The _system time_ is the number of seconds since the Unix epoch.

## Example

In zsh, type the following to see the current time in "seconds from the Unix epoch":

```bash
date +%s
```

Your results will vary, but it should be something greater than:

```bash
1663936403
```

The EpochConverter site[^1] is a fun way to explore dates in terms of the Unix epoch.

## Other Epochs

There are many different epochs for computing.
The wikipedia article[^2] on this topic has a table that includes the reasoning behind the choice.

Microsoft's .NET ecosystem sets its zero point at January 1st, 1 AD[^3].
Another difference in the .NET epoch is the interval.
Instead of seconds, it uses 100 nanosecond intervals called _Ticks_.

### .NET Example

In PowerShell find the current ticks from the epoch like this:

```powershell
(Get-Date).Ticks
```

The result is the number of ticks since the .NET epoch.
It should be larger than this:

```text
637995156088866950
```

## References

[^1]: EpochConverter [site](https://www.epochconverter.com)
[^2]: Wikipedia [article on Epoch (computing)](https://en.wikipedia.org/wiki/Epoch_(computing))
[^3]: .NET documentation on [date and time](https://learn.microsoft.com/en-us/dotnet/api/system.datetime?redirectedfrom=MSDN&view=net-6.0#quick-links-to-remarks-topics).
