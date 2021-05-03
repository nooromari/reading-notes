## Reading and Writing Files

**File Paths**
The file path is a string that represents the location of a file. 
- Folder Path: the file folder location on the file system
- File Name: the actual name of the file
- Extension: the end of the file path used to indicate the file type

### Opening and Closing a File in Python

- To open the file invoking the `open()` built-in function *containing the path to the file as an argument* will return the file object.

- To close the file use `close()` or `with open('filebame.txt') as reader:` followed by file processing(The with statement automatically takes care of closing the file once it leaves the with block, even in cases of error).

- use the second argument for `open()` to represent how you want to open the file. (*example `open('abc.txt', 'r')`*)

![modes](https://miro.medium.com/max/1090/0*CZMzQqblpb9It2IS)


### Exceptions 

- `raise` allows you to throw an exception at any time.
- `assert` enables you to verify if a certain condition is met and throw an exception if it isn’t.*use for test*
- In the `try` clause, all statements are executed until an exception is encountered.
- `except` catch and handle the exception(s) that are encountered in the try clause.
- `else`  run only when no exceptions are encountered in the try clause.
- `finally` enables you to execute sections of code that should always run, with or without any previously encountered exceptions.

![](https://hub.packtpub.com/wp-content/uploads/2019/12/image2.png)


**Built-in exceptions**

![](https://image.slidesharecdn.com/pythonprogrammingessentials-m21-exceptionhandling-140819043210-phpapp01/95/python-programming-essentials-m21-exception-handling-16-638.jpg?cb=1408424342)