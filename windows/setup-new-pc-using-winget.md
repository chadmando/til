# Setup New PC Using winget

Installing softare on a new Windows computer can be time consuming.
One method for installing softare is by [using winget](install-software-using-winget.md).
If you have an existing computer with a setup you would like to replicate, winget has an option to help.

## Use Winget To Export A List Of Software

On the old pc, run the command `winget export c:\temp\winget_pkgs.json`.
This creates creates a file similar to this:

[winget export example](https://gist.github.com/chadmando/130003c63120b14426afd1548112ab01)

## Use The JSON File To Install Software

Transfer the json file to the new pc. (c:\path\to\file\winget_pkgs.json)
Install software in the package file by running `winget import c:\path\to\file\winget_pkgs.json`.
