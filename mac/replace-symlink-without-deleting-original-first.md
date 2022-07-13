# Replace Symlink Without Deleting Original

A common problem when using Pycharm and updating Python using Homebrew is broken symlink in the virtural environments.
After upgrading Python using Homebrew, the binaries are in a new folder.
I grew tired of recreating new virtualenvs pointing to the new location.
I started looking around to see if I could update the symlinks because those seemed to be the only "broken" parts.
Stack Overflow to the rescue[^1].

## Solution

This is _a_ solution, not _the_ solution.

```bash
ln -s /path/to/new/python/bin newPython
mv newPython Python
```

[^1]: [Stack Overflow Question](https://stackoverflow.com/questions/1727280/is-there-a-way-to-edit-a-symlink-without-deleting-it-first)