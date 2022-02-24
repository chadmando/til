# Rename an existing branch

If your current branch is *master* and you want to rename it to *main*, use this command.

```bash
git branch -m master main
```

Note: You must have at least one commit on the master branch.
If you don't, you'll see this error message.

```bash
error: refname refs/heads/master not found
fatal: Branch rename failed
```

## Reference

Found in the git 2.26.0 manual.
To access the help:

```bash
git branch --help
```
