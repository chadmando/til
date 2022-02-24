# Get OS Version from Terminal

To find the macOS version from the terminal, use the `sw_vers` command.

```bash
$ sw_vers
ProductName:    macOS
ProductVersion: 11.6.4
BuildVersion:   20G417
```

The result is a set of key/value pairs.
You can directly access any *value* by using the *key* as a flag with the command.

```bash
$ sw_vers -productversion
11.6.4
```

## References

Found in the MACOS_Exploit section of [The Operator Handbook](https://www.amazon.com/Operator-Handbook-Team-OSINT-Reference/dp/B085RR67H5) by [Netmux](https://www.netmux.com/).
