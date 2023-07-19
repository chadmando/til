# AES-CBC Padding

To encrypt plaintext using Advanced Encryption Standard (AES) in Cipher Block Chaining (CBC) mode, the plaintext must be a multiple of 16 bytes long.
All plaintext is padded before encryption.
The padding method is described in Section 6.3 of [PKCS #7](https://www.rfc-editor.org/rfc/rfc5652).

## The Padding Technique

If the last block of the plaintext message has 1 byte (e.g., if the plaintext is 17, 33, or 49 bytes), then 15 bytes of the value 0x0f (15) are added to the end of the plaintext.
This can be evaluated using modulo math in python.

```python
plaintext = b"Thinking In Bytes"
len(plaintext) % 16
1
```

This operation gives the number of bytes in the last block.
In this example, the plaintext message _Thinking In Bytes_ has a length of 17 bytes, so 1 byte remains in the last block.
To determine which value to use for padding, the formula would look like this:

```python
BLOCKSIZE = 16
plaintext = b"Thinking In Bytes"
padding = BLOCKSIZE - len(plaintext) % BLOCKSIZE
```

The value of the padding is 15.
```python
padding
15
```

This pattern continues with other dangling bytes.
If the last block of the plaintext message has 2 bytes (e.g., the plaintext is 18, 34, 50… bytes), then 14 bytes of 0x0e (14) are added to the end of the plaintext.

## Do Perfect Plaintext Messages Get Padding?

The PKCS 7 standard says this:

> The padding can be removed unambiguously since all input is padded,
> including input values that are already a multiple of the block size,
> and no padding string is a suffix of another.

If the plaintext message is an exact multiple of the block size (e.g., 16, 32, 48...), `len(plaintext) % BLOCKSIZE == 0` then an additional 16 bytes of 0x00 (0) are added to the end. 
