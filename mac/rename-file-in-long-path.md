# Rename A File In A Long Path From The Terminal

## Common Approach

```bash
mv \long\path\to\file\.config \long\path\to\file\.config.old
```

## Better Approach

```bash
mv \long\path\to\file\{.config,.config.old}
```

## References

+ I discovered this in a [tweet](https://twitter.com/nixcraft/status/1508782292071686145) by [@nixcraft](https://twitter.com/nixcraft).
+ This [article](https://www.howtogeek.com/725657/how-to-use-brace-expansion-in-linuxs-bash-shell/) explains brace expansion with many examples.
