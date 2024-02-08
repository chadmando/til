# Four Types Of String Literals In PowerShell

```powershell
$single = 'Single quoted string literal'
$double = "Double quoted string literal"

$hereSingle = @'
Single
Quoted
Here-String
'@

$hereDouble = @"
Double
Quoted
Here-String
"@
```

## Single Versus Double Quoted

The key difference between single-quoted and double-quoted strings and here-strings is variable expansion.
When using double-quoted strings, any variables will be replaced (expanded) by their value.

```powershell
$count = 34
$str = "The count is $count"
$str
```

Results:
```text
The count is 34
```

In the book _Windows PowerShell In Action_, a note recommends using
single-quoted strings and single-quoted here-strings unless you need variable
expansion.
