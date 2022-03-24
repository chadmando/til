# Copy and Rename Files in a Folder

## Background

A set of files needs to be copied and renamed.
The filenames use the same structure, but one part needs to change. 
A common example is a business file that has the year in the name.
When the year changes, you need to _save as_ with the new year in the file's name.

## Make the Files For the Example

```powershell
@(1..3) | %{New-Item -Path ("./2021_file_" + $_ + ".txt") -ItemType File}
```

Creates these files:

```text
Name
----
2021_file_1.txt
2021_file_2.txt
2021_file_3.txt
```

## Copy and Rename the Files

You need to copy these files and change the year from 2021 to 2022.

```powershell
Get-ChildItem *.txt |
Select-Object -ExpandProperty Fullname |
Foreach-Object {Copy-Item -Path $_ -Destination ($_).replace("2021","2022")}
```

Now you'll have these files:

```text
Name
----
2021_file_1.txt
2021_file_2.txt
2021_file_3.txt
2022_file_1.txt
2022_file_2.txt
2022_file_3.txt
```
