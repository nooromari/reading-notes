## Modifying the Behavior of a Python Scope

* Python provides two keywords that allow you to modify the content of **global** and **nonlocal** names.

![](https://community.dataquest.io/uploads/default/original/1X/6385a29a0cc08eb5fad8382f721a868769a80dc8.png)

### The global Statement

when you try to assign a value to a global name inside a function, you create a new local name in the function scope.  you can define a list of names that are going to be treated as global names by use a global statement. 

The statement consists of the global keyword followed by one or more names separated by commas. You can also use multiple global statements with a name (or a list of names). All the names that you list in a global statement will be mapped to the **global** or module scope in which you define them.

![global](https://imgs.developpaper.com/imgs/202012090302626.jpg)


### The nonlocal Statement

With a nonlocal statement, you can define a list of names that are going to be treated as nonlocal.
*nonlocal names can be accessed from inner functions, but not assigned or updated.*

The nonlocal statement consists of the nonlocal keyword followed by one or more names separated by commas. These names will refer to the same names in the **enclosing** Python scope.