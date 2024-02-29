# Wipe A Drive Using Diskpart

Use these steps to wipe or clean any connected drive in Windows.
The [reference](#references) mentions Windows 10 but I have tested on Windows 11 too.

>[!Warning]
>Confirm the target disk before running the clean command.
>Running clean on the wrong disk may be catastrophic.

1. Launch the Diskpart utility; Win + R, then type `diskpart`
1. Use the `list disk` to see a list of mounted disks
1. Select the target disk using `select disk <disk num>`
1. Re-run `list disk` and confirm the target disk as an `*` next to it.
1. Run `clean` to clean the selected disk.

## References

Discovered through this [article](https://graspingtech.com/how-to-delete-all-partitions-from-a-disk-in-windows/).
