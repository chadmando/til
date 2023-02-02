# Find Configured DNS Servers Using CMD

Sometimes you want to know which server is configured for DNS.
Run this at a command prompt:

```cmd
ipconfig /all | findstr "DNS\ Servers"
```

