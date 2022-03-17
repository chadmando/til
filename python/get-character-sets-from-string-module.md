# Get Character Sets from the Python String Module

The `string` module from Python's standard library contains many sets of characters.
Before you build your own, look here first.

Start by importing the module

```python
import string
```

The help file lists the available sets.

+ whitespace -- a string containing all ASCII whitespace
+ ascii_lowercase -- a string containing all ASCII lowercase letters
+ ascii_uppercase -- a string containing all ASCII uppercase letters
+ ascii_letters -- a string containing all ASCII letters
+ digits -- a string containing all ASCII decimal digits
+ hexdigits -- a string containing all ASCII hexadecimal digits
+ octdigits -- a string containing all ASCII octal digits
+ punctuation -- a string containing all ASCII punctuation characters
+ printable -- a string containing all ASCII characters considered printable

## Exampmles

```python
string.ascii_uppercase
```

Returns a string with all of the uppercase ASCII characters.

```text
'ABCDEFGHIJKLMNOPQRSTUVWXYZ'
```

```python
string.hexdigits
```

```text
'0123456789abcdefABCDEF'
```

## References

+ Python documenation for the [string module](https://docs.python.org/3/library/string.html)
