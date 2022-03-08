# Get File Hash Using PowerShell

Use the `Get-FileHash` cmdlet to return a file's hash value.
Several hashing algorithms are available.
SHA256 is the default algorithm.

```powershell
Get-FileHash c:\temp\test.pdf
```

Resutls:

```text
Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA256          70DB569CD3FD842D963B04E6770B1606750D07A47396CB52BEAE2A3CE82360D8       C:\temp\test.pdf
```

Keep in mind that an object is returned.
One of the properties of the object is the _Hash_ value.

## Access the Hash Value

If you want to get _just_ the hash value, wrap the cmdlet in () and ask for the _Hash_ property.
This is handy when you trying to compare to a known good hash value.

```powershell
(Get-FileHash c:\temp\test.pdf).Hash
```

Results:

```text
70DB569CD3FD842D963B04E6770B1606750D07A47396CB52BEAE2A3CE82360D8
```

## Use a Different Algorithm

```powershell
Get-FileHash c:\temp\test.pdf -Algorithm SHA1
```

Output:

```text
Algorithm       Hash                                                                   Path
---------       ----                                                                   ----
SHA1            19759947501DEB5FCD1F2ADDF56C9D7CC19F2AFC                               C:\temp\test.pdf
```

## References

Consult the PowerShell help `Get-Help Get-FileHash -Full`.