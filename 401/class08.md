## List Comprehensions

It consists of brackets containing an expression followed by a for clause, then
zero or more for or if clauses. The expressions can be anything, meaning you can
put in all kinds of objects in lists.

The list comprehension always returns a result list.


### Syntax
The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the
result is going to be a list.

*result* = [*transform* *iteration* *filter* ]

**Example**:

`new_range = [i * i for i in range(5) if i % 2 == 0]`



![](https://miro.medium.com/max/858/0*ChFR2D9j8fxqz3D5.png)





