# Capture Network Traffic Across a Reboot

## Initial Conditions

+ Command prompt with Adminstator privileges
+ You want to save the capture data to `c:\temp\reboot-capture.etl`

## Start the Capture

Begin capture with this command.

```batchfile
netsh trace start persistent=yes capture=yes tracefile=c:\temp\reboot-capture.etl
```

Restart the computer.

## Stop the Capture

```batchfile
netsh trace stop
```

The capture file is an `etl` file type.
Use Microsoft's [etl2pcapng tool](https://github.com/microsoft/etl2pcapng) to analyze the capture in [Wireshark](https://www.wireshark.org/).

## References

Discovered in this [blog post](https://techcommunity.microsoft.com/t5/iis-support-blog/capture-a-network-trace-without-installing-anything-amp-capture/ba-p/376503).
