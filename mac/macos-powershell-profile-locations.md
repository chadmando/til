# macOS PowerShell Profile Locations

> Based on PowerShell v7.2.6
>
> Tested with `pwsh` launched from the terminal and VS Code


| Profile | Path To File |
| --- | --- |
| AllUsersAllHosts | /usr/local/microsoft/powershell/7/profile.ps1 |
| AllUsersCurrentHost | /usr/local/microsoft/powershell/7/Microsoft.PowerShell_profile.ps1 |
| CurrentUserAllHosts | $HOME/.config/powershell/profile.ps1 |  
| CurrentUserCurrentHost | $HOME/.config/powershell/Microsoft.PowerShell_profile.ps1 |

## Check Your $HOME Folder Path

To see your `$HOME` folder path use:

```powershell
$env:HOME
```

or

```bash
echo $HOME
```
