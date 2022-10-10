# Configure SSH Key To Work With GitHub

If you have added your public ssh key to your GitHub account, you may need to let ssh know which private key to use when working with github repos.

> NOTE
> This example is based in Windows.
> If you are working with Linux or macOS modify the `\` to a '/' accordingly.
>

## SSH Key Test

Many references use this test to verify your ssh key is working with GitHub.

```bash
ssh -T git@github.com
```

If this test fails, try the following to configure ssh to use the right private key.

## Create An SSH Config File

Assuming that you use the `$HOME\.ssh\` folder to store your keys, create a config file.

> If you already have an ssh config file, skip to the next step.

```powershell
New-Item ~\.ssh\config -ItemType File
```

## Add GitHub Configuration Details

Open the ssh config file in an editor and add this:

```text
Host github.com
    Hostname github.com
    User git
    IdentityFile C:\Users\<username>\.ssh\<name of your private key>
```

You may be able to use an aliased path like `~\.ssh\` or `$HOME\.ssh\` but I have not tested that approach. 
The full path has worked for me.

Now rerun the [ssh key test](#ssh-key-test) and it should give a success message like this:

```text

```