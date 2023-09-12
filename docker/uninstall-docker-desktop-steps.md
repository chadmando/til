# Uninstall Docker Desktop Steps

A recent support case with Docker resulting in an uninstall/reinstall of Docker Desktop.
The steps to uninstall Docker Desktop (Windows) are below.
The important part of the instructions is the clearing of all folders associated with the application.

```
1. Uninstall Docker Desktop

2. Delete the below files (note that the below commands are destructive, meaning it will delete all your images, volumes, and any Docker related files on your system)
C:\ProgramData\Docker
C:\ProgramData\DockerDesktop
C:\Program Files\Docker
C:\Users\<your user name>\.docker
C:\Users\<your user name>\AppData\Local\Docker
C:\Users\<your user name>\AppData\Roaming\Docker
C:\Users\<your user name>\AppData\Roaming\Docker Desktop

3. Reinstall Docker Desktop and see if this helps.
```
