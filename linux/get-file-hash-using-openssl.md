# Get File Hash Using OpenSSL

Use the `dgst` (for message _digest_) option in OpenSSL to find a file's hash.

## Create A File To Hash

```bash
touch .\myfile.txt
echo "Some text for my file." > .\myfile.txt
```

## Find The Hash Of The File

```bash
openssl dgst -sha256 .\myfile.txt
```

Results:

```text
SHA2-256(.myfile.txt)= 8f755b34004a3d8462c988f43c8fa53f099cc6ccadbf1575763c5a03b43a70cb
```

## List The Available Algorithms

The version of OpenSSL may determine which hashing algorithms are available.

To list the algorithms:

```bash
openssl dgst -list
```

To find your current version of openssl:

```bash
openssl version
```

## Discussion

These command should work on macOS, Linux, or Unix operating systems with OpenSSL installed.
