# Add a Glogal Git Alias

Git has a global configuration file, _.gitconfig_. 
The items in the global configuration file apply to all local git repositories.
This is a good place to add your favorite aliases.
Here are two that I like.

> Create global alias `s` for `status -s`

```zsh
git config --global alias.s status -s
```

> Create global alias `lg` for `log --oneline --decorate --all --graph`
```zsh
git config --global alias.lg log --oneline --decorate --all --graph
```

## References

+ Git documentation on [Aliases](https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases).
+ This [article](https://digitalfortress.tech/tips/create-global-gitconfig-git-alias/) covers the global git alias topic with good examples.
