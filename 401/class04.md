## Classes and Objects

**Classes**: are essentially a template to create your objects.
**Objects**: are an encapsulation of variables and functions into a single entity.
 *Objects get their variables and functions from classes.* 

![](https://www.codesdope.com/pa-images-bucket/courses/python/co4.jpg)


## Thinking Recursively

 A recursive function is a function defined in terms of itself via self-referential expressions.

 ![](https://www.edureka.co/blog/wp-content/uploads/2019/08/2019-08-06-12_31_29-Window.png)


## Pytest Fixtures and Coverage

- **fixtures**: some objects available to all of your tests those contain data you want to share across tests, or they might involve the network or filesystem.
In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition.

>  If your fixture uses "yield" instead of "return", pytest understands that the post-yield code is for tearing down objects and connections. And yes, if your fixture has "module" scope, pytest will wait until all of the functions in the scope have finished executing before tearing it down.

- **Coverage**

![](https://image.slidesharecdn.com/nanog77-nrfu-final-191101143732/95/automating-network-ready-for-use-with-pytest-23-638.jpg?cb=1572619261)