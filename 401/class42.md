## Dunder Methods

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__` or` __str__`.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len('string'). But an empty class definition doesn’t support this behavior out of the box:

```
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```

To fix this, you can add a `__len__` dunder method to your class:

```
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```

![](https://introcs.cs.princeton.edu/python/33design/images/SpecialMethodsFunctions.png)


## Iterators

- The two dunder methods `__iter__` and `__next__`, are the key to making a Python object iterable.

On more abstract terms, iterators provide a common interface that allows you to process every element of a container while being completely isolated from the container’s internal structure.

Whether you’re dealing with a list of elements, a dictionary, an infinite sequence or another sequence type—all of that is just an implementation detail. Every single one of these objects can be traversed in the same way by the power of iterators.

*Objects that support the `__iter__` and `__next__` dunder methods automatically work with for-in loops.*

![](https://www.bogotobogo.com/python/images/python_iterators/iterable-vs-iterator.png)


## Generators

- Generators look like regular functions but instead of using the return statement, they use **yield** to pass data back to the caller.

- Calling a generator function doesn’t even run the function. It merely creates and returns a generator object.

- The code in the generator function only executes when `next()` is called on the generator object.

- when a `return` statement is invoked inside a function, it permanently passes control back to the caller of the function. When a `yield` is invoked, it also passes control back to the caller of the function—but it only does so temporarily.

- Whereas a `return` statement disposes of a function’s local state, a `yield` statement suspends the function and retains its local state.

![](https://static.javatpoint.com/tutorial/es6/images/es6-generators.png)

