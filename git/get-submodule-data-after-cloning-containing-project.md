# Get Submodule Data After Cloning the Containing Project

Sometimes after cloning a project that has submodules, you find the submodule folders empty.
These two commands get that data.

```bash
git submodule init
```

Then,

```bash
git submodule update
```

## References

After struggling with this topic, I found this information in the book [Pro Git](https://www.amazon.com/Pro-Git-Scott-Chacon/dp/1484200772) by Scott Chacon and Ben Straub.
