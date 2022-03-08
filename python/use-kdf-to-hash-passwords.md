# Use Key Derivation Functions to Hash Passwords

Don't use BLAKE2 for salted hashing of passwords.
Standard cryptographic hashing functions are not suitable for password hashing because they are too fast.
Hash passwords using a special type of function called a _Key_ _Derivation_ _Function_ (KDF).

> KDFs use more compute resources, memory, or both.
> These features make brute force password cracking expense.

## Key Derivation Functions

+ Argon2 (Preferred)
+ Password–Based Key Derivation Function 2 (PBKDF2)

## Salt

The purpose of salt is to individualize results.

+ If two users had the same password, the salt ensures the hashes are difference.
+ Salt is not a secret and can be stored in plain text.
+ Salt is to hashing as initialization vector is to encryption.

Use `secrets.token_bytes()` to generate a unique salt.
More on using Python's [secrets module](./generate-crypto-safe-random-numbers.md) to generate random strings.

## References

+ Chapter 9 of [Full Stack Python Security](https://www.manning.com/books/full-stack-python-security) by Dennis Byrne covers password hashing.
+ [Argon2 Specification](https://github.com/P-H-C/phc-winner-argon2/blob/master/argon2-specs.pdf)
+ Details of how Argon2 became the recommend method as a result of a [Password Hashing Competition](https://www.password-hashing.net/)
