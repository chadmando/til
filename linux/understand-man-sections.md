# Understanding Man Page Sections

When you see a system function followed by a number in parenthesis, the number is referring to the man page section.

For example, this is a sentence from the book *SSH Mastery*[^1]:

>If ssh(1) or sshd(8) complains about a configuration, verify that you’re separating multiple entries correctly.

The *ssh(1)* and *sshd(8)* reference the command and the man page section.

## Sections

There are (8) man page sections[^2]:

1. General commands
1. System calls
1. Library functions covering C std library
1. Special files /dev and drivers
1. File formats
1. Games and screensavers
1. Misc
1. System admin commands and daemons

## Using Sections

I discovered there are is a `read` program and a `read` system call from Julia Evans[^3].
To access the man page for the `read` you want, include the section in the `man` command.

```bash
man 1 read
```

or

```bash
man 3 read
```

## References

[^1]: Lucas, Michael W. SSH Mastery: OpenSSH, PuTTY, Tunnels and Keys (IT Mastery) . Tilted Windmill Press. [Kindle Edition.](https://www.amazon.com/SSH-Mastery-OpenSSH-PuTTY-Tunnels-ebook/dp/B079NL1L9K/)
[^2]: Wikipedia [Man page](https://en.wikipedia.org/wiki/Man_page) article
[^3]: Julia Evans [man page](https://wizardzines.com/comics/man-pages/) from the *Bite Size Linux* zine.
