# Fix Docker Volume Invalid Mode Error

## Original Docker Volume Command

```bash
docker run -it --rm -v ${PWD}:/malware chadmando/dssuite
```

Returned this error:

```text
docker: Error response from daemon: invalid mode: /malware.
```


> UPDATE - This Fix Doesn't Solve the Problem
> 
> I confused silencing the error for fixing the problem.
> The error was gone but what I wanted, to mount the `PWD` to the
> container's `/malware`, folder wasn't happening.
> See _The Real Problem_ for the fix.

To fix the error, I found this [question](https://stackoverflow.com/questions/50540721/docker-toolbox-error-response-from-daemon-invalid-mode-root-docker) on Stack Overflow.
There are many opinions on how to fix the error.
I tried variations ~~until I found the minimal change required.~~

## Fixed Docker Volume Command 

```bash
docker run -it --rm -v '/${PWD}:/malware' chadmando/dssuite
```

~~The two changes that fixed the error:~~

+ ~~Add the front slash `/` before the `${PWD}`~~
+ ~~Enclose the entire volume argument in single quotes `'`~~

## The Real Problem

I want to mount the current working folder to the docker container's `/malware` folder.

## The Real Cause

I was using a `PSDrive` aliased path in PowerShell.

### Example

```powershell
New-PSDrive -Name "dev" -PSProvider FileSystem -Root C:\dev
```

```powershell
Set-Location dev:\
```

## Solution

I was at `dev:\` and trying to mount to the container.
It wasn't happening.
After starting the container, no files from the local folder were visible in the container.

Docker didn't like the aliased path `dev:\`.
I used `Covert-Path` to move back to the _Root_.

```powershell
Set-Location (Convert-Path $pwd)
```

This changed the $pwd to `C:\dev`.
Now the local folder mounts to the container. 
