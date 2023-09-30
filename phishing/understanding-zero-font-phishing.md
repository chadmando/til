# Understanding ZeroFont Phishing

ZeroFont phishing can be used to confuse users and email-protection services.

## What is ZeroFont Phishing

Including html text styled with a font size of 0 pixels.
This will make the text readable to machines but not to humans.

Example:
```html
Th<span style="FONT SIZE: 0px">Nonsense</span>ank y<span style="FONT SIZE: 0px">More Nonsense</span>ou
```

A human would see the example rendered as `Thank you`.
A machine would read it as `ThNonsenseank yMoreNonsenseou`.

## How Attackers Use ZeroFont Phising

Two tactics that have been reported are:

1. Confuse Ant-Phishing Filters.
Algorithms designed to spot spoofing attempts won't see company names that are obfuscated by this method.[^1]
2. Display fake *safe message* headers to convince users an email is safe.[^2]

## References

[^1]: https://www.avanan.com/blog/zerofont-phishing-attack
[^2]: https://isc.sans.edu/diary/A%20new%20spin%20on%20the%20ZeroFont%20phishing%20technique/30248
