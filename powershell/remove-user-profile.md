# Remove User Profile

To completely remove a user's profile, not just delete the user's folder, use the CIM command:

```powershell
# Replace 'UserA' with the username
Get-CimInstance -Class Win32_UserProfile |
Where-Object { $_.LocalPath.split('\')[-1] -eq 'UserA' } |
Remove-CimInstance
```

## References

Discovered on the Adam the Automator site.  Link [here](https://adamtheautomator.com/powershell-delete-user-profile/).