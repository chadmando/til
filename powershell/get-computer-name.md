# Get Computer Name

To get the computer's current name as a string to use for comparison use:

> Windows Only

```powershell
Get-CIMInstance -ClassName CIM_ComputerSystem | Select-Object -ExpandProperty Name
```
