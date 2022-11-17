# Microsoft SQL Installation Notes for Windows 10 Pro

These notes are for a common installation I perform and may not apply to all operating systems or version of MSSQL.

## Installation Log File Location

If there is an error during installation, a file called `Summary.txt` will be created.
The file is stored here:

```cmd
C:\Program Files(x86)\Microsoft SQL Server\100\Setup Bootstrap
```

## Dealing with Corrupted Peformance Counter Registry Hive

To ignore the check for a corrupted performance reference counter, install from an elevated CMD prompt:

```cmd
SQLEXPR.exe /ACTION=install /SKIPRULES=PerfMonCounterNotCorruptedCheck
```
