# Delete Merged Branches

The GitHub workflow can create a lot of branches in your git history.
After merging a local branch, delete it using `git branch -d <branch name>`.
When there are lots of local branches to delete, use the following command:

In bash or zsh:
```bash
git branch --merged | egrep --invert-match "^\*|main" | xargs git branch -d
```

Following a similar process in PowerShell:
```powershell
git branch --merged |
Select-String -NotMatch "^\*|main" |
Foreach-Object{$_.ToString().Trim()} |
Foreach-Object{Invoke-Expression "git branch -d $_"}
```

## Discussion

The bash version works in macOS and the PowerShell version works on Windows.
Git must be installed on the Windows computer.
The primary branch is named _main_.

### References

More on this method and how to clean up remote branches [here](https://devconnected.com/how-to-clean-up-git-branches).
