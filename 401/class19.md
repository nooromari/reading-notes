## Python Regular Expression

**Regular Expressions** (*regex*): are a sequence of characters used to check whether a pattern exists in a given text (string) or not. 

![](https://miro.medium.com/max/2964/1*hjsbL45MhT2Tw5DGAYoAUg.png)

- There is very useful functions provided by the `re` library, such as: compile(), search(), findall(), sub() for search and replace, split().

- The `match()` function checks for a match only at the beginning of the string (by default), whereas the `search()` function checks for a match anywhere in the string.


## shutil — High-level File Operations

- `copyfile()` copies the contents of the source to the destination and raises IOError if it does not have permission to write to the destination file.

- The implementation of `copyfile()` uses the lower-level function `copyfileobj()`. While the arguments to `copyfile()` are filenames, the arguments to `copyfileobj()` are open file handles. The optional third argument is a buffer length to use for reading in blocks.

- The `copy()` function interprets the output name like the Unix command line tool `cp`. If the named destination refers to a directory instead of a file, a new file is created in the directory using the base name of the source.

- `copy2()` works like `copy()`, but includes the access and modification times in the metadata copied to the new file.

- shutil includes three functions for working with directory trees. To copy a directory from one place to another, use `copytree()`. It recurses through the source directory tree, copying files to the destination. The destination directory must not exist in advance.