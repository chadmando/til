# Use Immediate Window To Evaluate Code

When workinging in VBA, the Immediate Window provides a way to run code without creating Subroutines.

In the Immediate Window, start the line with a Question Mark `?`.
```vba
` in Excel VBA you may want to find the value of cell A3
?Range("A3").Value
```

Press enter and the line will be evaluated.
Here the value in cell A3 is `13579`.

```vba
?Range("A3").Value
13579
```