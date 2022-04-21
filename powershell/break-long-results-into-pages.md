# Break Long Results Into Pages

When working in the console, some commands have output that runs many times the length of the window.
To break the output into managable chunks, pipe the results to `more` or `Out-Host -Paging`.

```powershell
Get-Service | more
```

or 

```powershell
Get-Service | Out-Host -Paging
```

## Keyboard Commands To Control Paging

| Key | Action |
| --- | --- |
| Space | Show next page of results |
| Enter | Show next result |
| Q | Quit showing results |

