# Access Environment Variable is VBA

Call the `Environ` function with the name of the environment variable.[^1]

```vba
Environ("USERPROFILE")
```

Returns:

```text
C:\Users\<username>
```

The environment variable can also be accessed by index number instead of by name.

[^1]: Microsoft Docs on the Environ function [here](https://docs.microsoft.com/en-us/office/vba/language/reference/user-interface-help/environ-function)