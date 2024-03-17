# Find Imported Music Files In macOS

## Initial Conditions

+ Music Version 1.4.x
+ macOS Version 14.4

## Finding The Files

After importing music files into the _Music_ application, you may need to find the original files.
Especially if you want to remove the music from your Library.
Using the `Delete From Library` option state that the music will be removed from your Library but the original imported files will not be deleted.

The files are located in a subfolder at this path:

```bash
~/Music/Music/Media/<name of imported album>
```

A full path would look like:

```bash
/Users/<UserName>/Music/Music/Media/<name of imported album>
```
