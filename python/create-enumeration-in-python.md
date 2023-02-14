# Create Enumeration In Python

To create an enumeration in Python, create a class that inherits from enum.Enum.

```python
from enum import Enum

class Directions(Enum):
    UP = 'i'
    DOWN = 'm'
    RIGHT = 'k'
    LEFT = 'j'

```

Enumerations contains constants called _members_.
Each member has a _name_ and a _value_.
Access the value using dot notation or similar to a dictionary.

```python
Directions['RIGHT']
<Directions.RIGHT: 'k'>
```

or

```python
Directions.RIGHT
<Directions.RIGHT: 'k'>
```

To access just the value, add a `.value`:

```python
Directions.RIGHT.value
'k'
```

To access just the name of the member:

```python
Directions.RIGHT.name
'RIGHT'
```

There are other classes in the enum module the are designed for specific behavior.

+ IntEnum: The members can be used anywhere you would use an `int` type.
+ StrEnum: The members can be used anywhere you would use a `str` type.
+ Flag: The members can be combines using Bitwise Operators.

Member values can be assigned automatically using `auto()` as the value in the class definition.
