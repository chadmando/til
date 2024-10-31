# Split and Join Multiline String

When working with strings that represent a file path in PowerShell, it is useful to remove the "file" portion of the string and leave just the directory.

When working with paths that are strings, the normal path methods aren't available (i.e. `PSParentPath`)

Given this string.

```powershell
$string = "C:\Users\chadmando\\Projects\Customer\Big Major Project\Special Folder\CONFIDENTIAL.xlsm"
```

To remove the last portion (CONFIDENTIAL.xlsm), first split the string on the `\` character.

```powershell
# Split the string on the backslash
$splitString = $string.split('\')
```

Then, reassemble the string without the last element from the split.

```powershell
# Remove the last element and reassemble the path
$newString = ($splitString[0..($splitString.Count - 2)] -join '\')
```
