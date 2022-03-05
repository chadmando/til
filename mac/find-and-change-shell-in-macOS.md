# Find and Change Shell in macOS

Find your current shell.

```zsh
echo $0
```

Or, enter a gibberish command.

```zsh
chadmando
```

The unknown command will return the name of the shell with a _command not found_ error.

```zsh
zsh: command not found: chadmando
```

Change shells using the `chsh` command.

```zsh
chsh -s $(which bash)
```

## References

This [article](https://www.moncefbelyamani.com/which-shell-am-i-using-how-can-i-switch/) covers this topic and more about shells in macOS.
