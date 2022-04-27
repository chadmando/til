# Get WSMan Trusted Hosts

Use the `Get-Item` command to show the list of trusted hosts on a Windows machine.

> Elevated prompt required.

```powershell
(Get-Item WSMan:\localhost\Client\TrustedHosts).Value
```

Use the WSMan PSProvider.
If you need to add to the list of Trusted Hosts, save the current list in a variable.

```powershell
$base = (Get-Item WSMan:\localhost\Client\TrustedHosts).Value
```

Then append the value and include the `$base`.

```powershell
Set-Item WSMan:\localhost\Client\TrustedHosts -Value "$base,<your new hosts>"
```





