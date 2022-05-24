# Change Hostname On Raspbian

Change the hostname in two locations to rename a Raspberry Pi running Raspbian.

```bash
/etc/hostname
```

Launch the editor as `sudo`.

```bash
sudo nano /etc/hostname
```

In the hostname file, replace the current hostname with the new hostname.
Here you are just replacing what exists with what you want.
You must also make a change to this file:

```bash
/etc/hosts
```

Again, start your editor as `sudo`.

In the `/etc/hosts` file, change the name after the entry for `127.0.0.1`.
