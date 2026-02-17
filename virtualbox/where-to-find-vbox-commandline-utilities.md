# Where To Find VirtualBox Command Line Utilities

VirtualBox has additional utilities and some can run from the command line.
On Windows, find these in this folder `C:\Program Files\Oracle\VirtualBox\`

Here is a listing of the executables the folder:

```text
vbox-img.exe
VBoxAudioTest.exe
VBoxAutostartSvc.exe
VBoxBalloonCtrl.exe
VBoxBugReport.exe
VBoxDTrace.exe
VBoxExtPackHelperApp.exe
VBoxHeadless.exe
VBoxManage.exe
VBoxNetDHCP.exe
VBoxNetNAT.exe
VBoxSDS.exe
VBoxSVC.exe
VBoxTestOGL.exe
VBoxWebSrv.exe
VirtualBox.exe
VirtualBoxVM.exe
```

Locating the `VBoxManage.exe` utility was the reason for creating this til.
This utility allows the conversion from a `.img` file created with `dd` to a `.vdi` file that can be used to create a VM.

```cmd
.\vboxmanage.exe convertfromraw "E:\path\to\windows_image.img" "E:\path\to\windows_image.vdi" --format VDI --variant Standard
```
