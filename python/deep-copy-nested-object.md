# Deep Copy a Nested Object

To create an independent copy of a nested object, use the deepcopy method from the copy module.

```python
>>> obj = [['a','b','c'],['d','e','f'],['g','h']]
>>> import copy
>>> deep_copy = copy.deepcopy(obj)
>>> deep_copy
[['a', 'b', 'c'], ['d', 'e', 'f'], ['g', 'h']]
>>> deep_copy is obj
False
>>>
```

Setting objects equal will normally create a shallow copy.

```python
>>> obj = [['a','b','c'],['d','e','f'],['g','h']]
>>> shallow_copy = obj
>>> shallow_copy
[['a', 'b', 'c'], ['d', 'e', 'f'], ['g', 'h']]
>>> shallow_copy is obj
True
>>>
```

Any changes to the object that were a part of the operation that created `shallow_copy` will be shared between both variables.  Both `obj` and `shallow_copy` point to the same objects in Python.

## References

Found in Section 4.4 pf the book [Python Tricks The Book](https://realpython.com/products/python-tricks-book/) by Dan Bader.
