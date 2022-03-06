# Create Cryptographically Safe Random Strings Using the Secrets Module

Python has a module named _secrets_ that has several methods for generating random numbers.
The module documentation says the secrets module should be prefered over the _random_ module in security and cryptographic applications.

## The Token Functions 

The secrets module has three functions to generate random strings.

+ token_bytes() : Returns a random byte string
+ token_hex() : Returns a random string, in hexadecimal characters only
+ token_urlsafe() : Returns a random string that is safe to use in a random URL, in Base64 characters only

## Examples

Let python determine the length of the output.

```python
import secrets
secrets.token_hex()
```

The result would be something like:
```python
'c27ace177d5710234c3281906c2d813a5af74f3f038dadf9047f1e516c6976ac'
```

You can specify the length, in bytes, of the output.

```python
import secrets
secrets.token_bytes(16)
```

Result:

```python
'943c3e81dc3715894be869f27443c08c'
```

## References

+ Python secrets module [documentation](https://docs.python.org/3/library/secrets.html)
+ Discovered in the book [Full Stack Python Security](https://www.manning.com/books/full-stack-python-security) by Dennis Byrne.
