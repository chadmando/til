# Remove Tracked File from Git

If a file is being tracked and needs to be removed from the working tree, use this command:

```bash
git rm --cached <file>
```

The file should be added to .gitignore otherwise you may find yourself in a vicious cycle.

## References

I found the solution in this Stack Overflow [question](https://stackoverflow.com/questions/1274057/how-do-i-make-git-forget-about-a-file-that-was-tracked-but-is-now-in-gitignore).
