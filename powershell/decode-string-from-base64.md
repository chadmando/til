# Decode String From Base64

This [article](https://www.sans.org/blog/month-of-powershell-profile-hack-base64-encoding-decoding/) provides a nice breakdown for the process of decoding Base64 to a string.
It also gives a clean way to setup a function in your PowerShell profile to handle this task.
You have options for the type of string encoding such as Unicode, UTF-8, UTF-7, or ASCII.

```powershell
[System.Text.Encoding]::Unicode.GetString([System.Convert]::FromBase64String($EncodedText))
```

or

```powershell
[System.Text.Encoding]::UTF8.GetString([System.Convert]::FromBase64String($EncodedText))
```

or

```powershell
[System.Text.Encoding]::ASCII.GetString([System.Convert]::FromBase64String($EncodedText))
```

## Example

## References
