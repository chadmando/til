# Get Member Of .NET Class Without An Instance

To explore the properties and methods of a .NET Class that doesn't have a constructor use the `-Static` parameter with `Get-Member`.

```powershell
[System.Environment] | Get-Member -Static
```

## Discovery

A quick review of how I learned this.
When trying to explore the member of the `System.Environment` .NET class I started with `Get-Member`.
If you try to pipe `[System.Environment]` to `Get-Member` you get the members for `TypeName: [System.RuntimeType]`.

```powershell
[System.Environment] | Get-Member
   
   TypeName: System.RuntimeType

Name                                  MemberType Definition
----                                  ---------- ----------
AsType                                Method     type AsType()
Clone                                 Method     System.Object Clone(), System.Object ICloneable.Clone()
Equals                                Method     bool Equals(System.Object obj), bool Equals(type o)
```

That wasn't what I was looking for.
My next thought was to make a new instance of the [System.Environment] class.

```powershell
$foo = New-Object System.Environment
New-Object: A constructor was not found. Cannot find an appropriate constructor for type System.Environment.
```

`System.Environment` doesn't have a constructor, it is just a .NET Class.  
At this point, I was out of ideas.
I posted the question on the PowerShell Discord and the helpful folks there pointed me to the `-Static` parameter.
To see the properties and methods of a class that doesn't have a constructor, pipe to `Get-Member -Static`.


```powershell
[System.Environment] | Get-Member -Static

   TypeName: System.Environment

Name                       MemberType Definition
----                       ---------- ----------
Equals                     Method     static bool Equals(System.Object objA, System.Object objB)
Exit                       Method     static void Exit(int exitCode)
ExpandEnvironmentVariables Method     static string ExpandEnvironmentVariables(string name)
FailFast                   Method     static void FailFast(string message), static void FailFast(string message...
GetCommandLineArgs         Method     static string[] GetCommandLineArgs()
```

You can see above, the members of the `TypeName: System.Environment` are being returned.

## `-Static` Documentation

To close the loop on understanding, I read through the help and I was clearly stated.


> Indicates that this cmdlet gets only the static properties and methods of the object. 
> Static properties and methods are defined on the class of objects, not on any particular instance of the class.