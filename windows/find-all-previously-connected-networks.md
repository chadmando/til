# Find All Previously Connected Networks

> Accessing this Registry location using PowerShell requires elevated privileges (run as Adminstrator).

Registry location to look for all previous networks:

```text
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\NetworkList\Profiles
```

Additional information in the Registry Key:

+ ProfileName
+ Description
+ Managed
+ Category
+ DateCreated
+ NameType
+ DateLastConnected


## References

This [article](https://www.weaklink.org/2016/11/windows-network-profile-registry-keys/) is one of many when searching for answers on this topic.
