# Show Completion Options in PowerShell

Using tab completions is a great way to reduce typing and mistakes when working in PowerShell.
Typically you start typing the first few letters of a cmdlet or parameter and press Tab to invoke the magic.
Sometimes you want to know which parameters are availabe without starting to type or without using `Get-Help`.

To see available options use these key combinations.

## Completion Options on Windows

> Ctrl + Space

## Completion Options on macOS

> Tab Tab (press twice)

## Example

Type `Get-Process -` then use the completion options key combination above.

Result on macOS:

```text
PS /Users/chadmando/example> Get-Process -
Name                 IncludeUserName      Verbose              WarningAction        WarningVariable      OutBuffer            
Id                   Module               Debug                InformationAction    InformationVariable  PipelineVariable     
InputObject          FileVersionInfo      ErrorAction          ErrorVariable        OutVariable          
PS /Users/chadmando/example> Get-Process -
```

You get all of the possible parameters that can be used with `Get-Process`.

> NOTE: the `-` after the cmdlet is important.

The best part of this this feature is that it restores what you typed before invoking it.
Notice in the results how `Get-Process -` at the new prompt is part of the output?

## Requirements

The PSReadLine module is required.
Confirm you have it imported in the current session by running `Get-Module PSReadLine`.

### Investigate More Key Combination Shortcuts

`Get-PSReadLineKeyHandler`

## References

+ I heard about Ctrl+Space on the [Stop Typing So Much](https://www.podbean.com/ew/pb-xvf99-11e01aa) episode of The PowerShell Podcast.
+ When it didn't work on macOS, I found this reddit [post](https://www.reddit.com/r/PowerShell/comments/tlvhpn/ctrlspace_on_macos/).
