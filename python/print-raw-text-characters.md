# Print Raw Text Characters Without Rendering

While attempting to rename screenshot files in macOS using node or python, copying the filename from `ls` and using that for a move operation fails.
The issue is that macOS (tested on Tahoe) uses a narrow no break space(`\u202f`)[^1] between the time and the *AM* or *PM*.

Find the non-standard space by wrapping the `repr()` command with `print()`:

```python
import os

D = "/path/to/files"
files = os.listdir(D)

for f in sorted(files):
    print(repr(f))
```

## Reference

[^1]: Unicode reference chart [PDF document](https://www.unicode.org/charts/PDF/U2000.pdf)