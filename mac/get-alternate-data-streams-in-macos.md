# Get Alternate Data Streams In macOS

Windows files can contain Alternate Data Streams (ADS).
There are ways view the ADS information in Windows [see the Zone Identifier til](../powershell/show-zone-identifier-for-all-files-in-downloads-folder.md).
You can view the ADS in macOS or Linux by two methods.

## View extended attributes using `ls`

When listing files use the `-@` option to display extended attributes.

```bash
ls -l@
```

## Use the `xattr` command

Use the `xattr` command with the `-l` option to see the ADS and its contents.

```bash
xattr -l <file_you_are_investigating.ext>
```

## References

This [blog post](https://www.jankyrobotsecurity.com/2018/07/24/accessing-alternate-data-streams-from-a-mac/) has a more detailed explaination of these two methods.
