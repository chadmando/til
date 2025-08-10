# View or List USB Storage In Terminal

In macOS, mounted USB storage media can be found in the `/Volumes` directory.
To list the mounted volumes:

```bash
ls -l /Volumes
```

You will see your system Volume, something like _Macintosh HD_, and any other mounted Volumes.
For Example:

```bash
total 544
lrwxr-xr-x  1 root     wheel       1 Aug  5 13:27 Macintosh HD -> /
drwx------@ 1 root  staff  262144 Dec 31  1969 One Touch
drwx------@ 1 root  staff       0 Dec 27  1970 SCANNER
```

In this example, both `One Touch` and `SCANNER` are external USB storage devices.
Those can be explored by using `ls`.

```bash
ls -l /Volumes/"One Touch" #Handle spaces in the name by using quotes
```

or

```bash
ls -l /Volumes/SCANNER #no spaces means no quotes needed
```
