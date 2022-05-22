# Text Or File Input Pattern For Argparse

Use this pattern for a positional argument that can be command line text or a file.

```python
import argparse
import os

def get_args():
    """Get command-line arguments"""

    parser = argparse.ArgumentParser(
        description='My Tools and Scripts',
        formatter_class=argparse.ArgumentDefaultsHelpFormatter)

    parser.add_argument('text',
                        metavar='text',
                        help='Input text or file')

    args = parser.parse_args()

    if os.path.isfile(args.text):
        args.text = open(args.text).read().rstrip()

    return args
```

## Usage

Text may be provided as an argument or by pointing to a file.

```bash
.\script.py "argument text"
```

or 

```bash
.\script.py .\argument.txt
```

### References

The book [_Tiny Python Projects_](http://tinypythonprojects.com/) by Ken Youens-Clark is an excellent resource for learning how to use Argparse. 
This pattern is borrowed from the book.
