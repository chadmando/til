# Deep Copy Nested Objects in PowerShell

Use the .NET PSSerializer class to deep copy some nested objects.
Objects must be [serialized](../concepts/understand-serialize-versus-deserialize.md) then deserialized to create the deep copy.
Some objects types do not serialize in a predictable manner.

```powershell
[Management.Automation.PSSerializer]
```

## Example

```powershell
$arr1 = @(1..3)
$arr2 = @(4..6)
$arr3 = @($arr1, $arr2)
$arr3
```

The variable `$arr3` contains both `$arr1` and `$arr2`.

```text
1
2
3
4
5
6
```

To create the deep copy:

```powershell
$arr4 = [Management.Automation.PSSerializer]::Deserialize([Management.Automation.PSSerializer]::Serialize($arr3))
$arr1[0] = "a"
$arr3
```

The `$arr3` is updated with the change made to `$arr1`

```text
a
2
3
4
5
6
```

```powershell
$arr4
```

The deep copy created, `$arr4`, is not changed.

```text
1
2
3
4
5
6
```

## References

I found the technique in this [article](https://stuart-moore.com/deep-copy-nested-arrays-in-powershell) by Stuart Moore.
