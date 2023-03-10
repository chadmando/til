# Personal.xlsb File Location

Standard location for the personal.xlsb file is:

```text
C:\Users\\[User Name]\AppData\Roaming\Microsoft\Excel\XLSTART
```

You can check the location by opening the Visual Basic IDE and Selecting a Module under the Personal.xlsb file.
Then, in the Immediate Window, type the following:

```vba
?ThisWorkbook.Path
```

The output will tell you where the personal.xlsb file is stored.
