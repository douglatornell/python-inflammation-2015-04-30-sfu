---
layout: page
title: Programming with Python
subtitle: Key Points
---
## [Analyzing Patient Data](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/01-numpy.ipynb)

*   Import a library into a program using `import libraryname`.
*   Use the `numpy` library to work with arrays in Python.
*   Use `variable = value` to assign a value to a variable in order to record it in memory.
*   Variables are created on demand whenever a value is assigned to them.
*   Use `print something` to display the value of `something`.
*   The expression `array.shape` gives the shape of an array.
*   Use `array[x, y]` to select a single element from an array.
*   Array indices start at 0, not 1.
*   Use `low:high` to specify a slice that includes the indices from `low` to `high-1`.
*   All the indexing and slicing that works on arrays also works on strings.
*   Use `# some kind of explanation` to add comments to programs.
*   Use `array.mean()`, `array.max()`, and `array.min()` to calculate simple statistics.
*   Use `array.mean(axis=0)` or `array.mean(axis=1)` to calculate statistics across the specified axis.
*   Use the `pyplot` library from `matplotlib` for creating simple visualizations.

## [Creating Functions](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/02-func.ipynb)

*   Define a function using `def name(...params...)`.
*   The body of a function must be indented.
*   Call a function using `name(...values...)`.
*   Numbers are stored as integers or floating-point numbers.
*   Integer division produces the whole part of the answer (not the fractional part).
*   Each time a function is called, a new stack frame is created on the **call stack** to hold its parameters and local variables.
*   Python looks for variables in the current stack frame before looking for them at the top level.
*   Use `help(thing)` to view help for something.
*   Put docstrings in functions to provide help for that function.
*   Specify default values for parameters when defining a function using `name=value` in the parameter list.
*   Parameters can be passed by matching based on name, by position, or by omitting them (in which case the default value is used).

## [Repeating Actions with Loops](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/03-loop.ipynb)

*   Use `for variable in collection` to process the elements of a collection one at a time.
*   The body of a for loop must be indented.
*   Use `len(thing)` to determine the length of something that contains other values.

## [Storing Multiple Values in Lists](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/03-loop.ipynb)

*   `[value1, value2, value3, ...]` creates a list.
*   Lists are indexed and sliced in the same way as strings and arrays.
*   Lists are mutable (i.e., their values can be changed in place).
*   Strings are immutable (i.e., the characters in them cannot be changed).

## [Analyzing Data in Multiple Files](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/03-loop.ipynb)

*   Use `glob.glob(pattern)` to create a list of files whose names match a pattern.
*   Use `*` in a pattern to match zero or more characters, and `?` to match any single character.

## [Making Choices](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/04-cond.ipynb)

*   Use the `ImageGrid` class from the `ipythonblocks` library to create simple "images" made of colored blocks.
*   Specify colors use (red, green, blue) triples, each component of which is an integer in the range 0..255.
*   Use `if condition` to start a conditional statement, `elif condition` to provide additional tests, and `else` to provide a default.
*   The bodies of the branches of conditional statements must be indented.
*   Use `==` to test for equality.
*   `X and Y` is only true if both X and Y are true.
*   `X or Y` is true if either X or Y, or both, are true.
*   Zero, the empty string, and the empty list are considered false; all other numbers, strings, and lists are considered true.
*   Nest loops to operate on multi-dimensional data.
*   Put code whose parameters change frequently in a function, then call it with different parameter values to customize its behavior.

## Errors and Exceptions

*   Tracebacks can look intimidating, but they give us a lot of useful information about what went wrong in our program, including where the error occurred and what type of error it was.
*   An error having to do with the "grammar" or syntax of the program is called a `SyntaxError`. If the issue has to do with how the code is indented, then it will be called an `IndentationError`.
*   A `NameError` will occur if you use a variable that has not been defined (either because you meant to use quotes around a string, you forgot to define the variable, or you just made a typo).
*   Containers like lists and dictionaries will generate errors if you try to access items in them that do not exist. For lists, this type of error is called an `IndexError`; for dictionaries, it is called a `KeyError`.
*   Trying to read a file that does not exist will give you an `IOError`. Trying to read a file that is open for writing, or writing to a file that is open for reading, will also give you an `IOError`.
