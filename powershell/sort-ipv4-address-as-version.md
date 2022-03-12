# Sort IPv4 Addresses as Version

Use the Scriptblock `{$_ -as [version]} to sort an array of IPv4 addresses.

Running these commands should result in a sorted list.

```powershell
$ips = @("192.168.5.25","192.168.5.1","192.168.6.18","192.168.5.10")
$ips | Sort-Object {$_ -as [version]}     
```

Results:

```text
192.168.5.1
192.168.5.10
192.168.5.25
192.168.6.18
```

## References

+ This method and many others are summarized in this ISC [Diary](https://isc.sans.edu/forums/diary/Sorting+Things+Out+Sorting+Data+by+IP+Address/27916/) by Rob VandenBrink.
+ Rob's write-up was in inspired by this [thread](https://twitter.com/flakpaket/status/1445419600624095236) on Twitter.
