# Create A File With All Installed Brew Packages

After searching for ways to speed up a new macOS setup, I discovered `brew bundle`.

Homebrew is required.
If you don't have Homebrew installed, why would you need to create a package listing?
To create a file with a listing of all installed brew packages run:

```bash
brew bundle dump
```

This command creates a file named `Brewfile` in the current folder.
It is common practice to save with your dotfiles, usually in your 'HOME' folder.

```bash
brew bundle dump --file ~/Brewfile
```

On a new macOS setup, after Homebrew is installed, you can install from the Brewfile using:

```bash
brew bundle install
```

## Example Dump File

Here is my [Brewfile](https://github.com/chadmando/dotfiles/blob/main/Brewfile).

## References

+ Internet search for `brew bundle` will give lots of examples.
+ A detailed write up of brew and brew bundle found [here](https://gist.github.com/ChristopherA/a579274536aab36ea9966f301ff14f3f).
+ Reading the help by running `brew bundle --help`.
