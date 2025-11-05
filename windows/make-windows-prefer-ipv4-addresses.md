# How To Make Windows Prefer IPv4 Addresses

On newer Windows 11 installations, Windows may default to IPv6 addressing.
This may cause issues if the local networking has IPv6 disabled.

This occurred during an attempt to install Microsoft 365 desktop apps.
The installation failed and Procmon events showed attempts to connect TCP to IPv6 addresses.

To prefer IPv4 over IPv6 make this registry edit:

```cmd
reg add HKLM\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters /v DisabledComponents /t REG_DWORD /d 0x20 /f
```

This change requires a restart.
After the restart, confirm the change by running:

```pwsh
Get-ItemProperty -Path HKLM:\SYSTEM\CurrentControlSet\Services\Tcpip6\Parameters |
Select DisabledComponents
```

Results should be:

```cmd
DisabledComponents : 32
```
