# How To Enroll A New PC in AutoPilot from OOBE

## Assumptions

1. You have a new, Windows 11, PC at the Out-Of-Box-Experience (OOBE)
1. Your organization has an Intune subscription
1. You have EntraID permissions to add a device to AutoPilot (e.g. Intune Administrator)
1. You have an USB storage device to save the Diagnostic logs

## Steps

1. Boot new PC to the OOBE
1. Enter Diagnostics mode `Ctrl` + `Alt` + `D`
1. Export Logs to USB Storage
1. Identify the device hash `csv` file in the exported logs
1. Login to Intune
1. Navigate to Devices->Windows->Enrollment->AutoPilot Enrollment
1. 




## References

[^1]: Microsoft documentation [page](https://learn.microsoft.com/en-us/autopilot/add-devices)
