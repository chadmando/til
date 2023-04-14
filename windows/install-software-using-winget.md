# Install Software Using Winget

Winget is Microsoft's Package Manager command-line tool.
It is enabled as a part of the _App Installer_ package.
App Installer is available through the Microsoft Store [here](https://apps.microsoft.com/store/detail/app-installer/9NBLGGH4NNS1?hl=en-us&gl=us&rtc=1).

## Winget Help

Winget uses the standard `--help`.

```cmd
winget --help
```

You'll see the basic commands:

```text
Windows Package Manager v1.4.10173
Copyright (c) Microsoft Corporation. All rights reserved.

The winget command line utility enables installing applications and other packages from the command line.

usage: winget  [<command>] [<options>]

The following commands are available:
  install    Installs the given package
  show       Shows information about a package
  source     Manage sources of packages
  search     Find and show basic info of packages
  list       Display installed packages
  upgrade    Shows and performs available upgrades
  uninstall  Uninstalls the given package
  hash       Helper to hash installer files
  validate   Validates a manifest file
  settings   Open settings or set administrator settings
  features   Shows the status of experimental features
  export     Exports a list of the installed packages
  import     Installs all the packages in a file

For more details on a specific command, pass it the help argument. [-?]

The following options are available:
  -v,--version              Display the version of the tool
  --info                    Display general info of the tool
  -?,--help                 Shows help about the selected command
  --wait                    Prompts the user to press any key before exiting
  --verbose,--verbose-logs  Enables verbose logging for WinGet
  --disable-interactivity   Disable interactive prompts
```

## Winget Search

To find an application to install, use the `search` command.
For example, to search for python 3.11 use the following command.

```cmd
winget search python
```

You would see results similar to this:

```text
Name                                     Id                                 Version      Match           Source
----------------------------------------------------------------------------------------------------------------
Python 3.10                              9PJPW5LDXLZ5                       Unknown                      msstore
Python 3.11                              9NRWMJP3717K                       Unknown                      msstore
Python 3.9                               9P7QFQMJRFP7                       Unknown                      msstore
Python 3.8                               9MSSZTT1N39L                       Unknown                      msstore
Python 3.7                               9NJ46SX7X90P                       Unknown                      msstore
Python 3.12 (Alpha)                      9NCVDN91XZQP                       Unknown                      msstore
计算机二级 Python 考试题库                  9PBKTNDS9VSH                       Unknown                      msstore
Learn Django and Python by GoLearningBus 9WZDNCRDN82R                       Unknown                      msstore
Python 3                                 Python.Python.3.9                  3.9.13       Command: python winget
Python 3                                 Python.Python.3.12                 3.12.0a5     Command: python winget
Python 3.11                              Python.Python.3.11                 3.11.3       Command: python winget
Python 3.10                              Python.Python.3.10                 3.10.10      Command: python winget
Python 2                                 Python.Python.2                    2.7.18150    Command: python winget
Miniconda3                               Anaconda.Miniconda3                py39_4.10.3  Command: python winget
winpython-pypy                           winpython.winpython-pypy           3.8.12.3     Tag: python     winget
winpython-dot-pypy                       winpython.winpython-dot-pypy       3.8.12.3     Tag: python     winget
winpython-dot                            winpython.winpython-dot            3.10.5.0     Tag: python     winget
winpython                                winpython.winpython                3.10.5.0     Tag: python     winget
Orange                                   UniversityofLjubljana.Orange       3.31.1       Tag: python     winget
pyzo                                     ThePyzoteam.pyzo                   4.12.4       Tag: python     winget
Stackless Python                         stackless.stackless                3.7.9150.0   Tag: python     winget
Spyder                                   Spyder.Spyder                      5.4.3        Tag: python     winget
SABnzbd                                  SABnzbdTeam.SABnzbd                3.7.2        Tag: python     wingetwing
```

## Winget Install

If you want to install Python 3.11.x you have two options.
One is sourced from the _msstore_ and the other from _winget_.
To install from the winget source, use the `Id` to specify the right python 3.11.

```cmd
winget install -Id Python.Python.3.11 --scope user
```

## Winget Upgrade

When updates to python 3.11 are released, upgrade with this command.

```cmd
winget upgrade -q Python.Python.3.11
```
