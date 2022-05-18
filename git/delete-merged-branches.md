# Delete Merged Branches

The GitHub workflow can create a lot of branches in your git history.
After a local branch is merged, it can be deleted using the `git branch -d <branch name>`.
When there are lots of local branches to delete, use the following command:

```bash
git branch --merged | egrep --invert-match "^\*|main" | xargs git branch -d
```

## Discussion

This works in macOS but not on Windows.
The primary branch is named _main_.

### References

More on this method and how to clean up remote branches [here](https://devconnected.com/how-to-clean-up-git-branches).
