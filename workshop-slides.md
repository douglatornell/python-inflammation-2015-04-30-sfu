---
layout: slides
title: Building Programs with Python
subtitle: Lessons
---

## Introduction

For our Python introduction we're going to pretend to be a researcher named Harold Bridge `hbridge` who is studying inflammation in patients who have been given a new treatment for arthritis.

The data we'll analyze is in the `python-inflammation/` directory of the data zip-file or you can download it from:

[https://bitbucket.org/douglatornell/swc-hbridge-files/downloads](https://bitbucket.org/douglatornell/swc-hbridge-files/downloads)


## Launching IPython Notebook - 1

There are several ways that we can use Python.
We're going to start with a tool called IPython Notebook (aka Jupyter) that runs in the browser.

In a shell window enter these commands:

~~~ {.bash}
$ cd python-inflammation
$ ipython notebook
~~~


## Launching IPython Notebook - 2

That shell window is now running a local web server for you.
Don't close it.
You will need to open another shell window to do other command-line things.

Your browser should open to an `jupyter` page showing a list of `inflamation-*.csv` files.
If it doesn't,
Open a new tab and enter the address `127.0.0.1:8888`.


## Analyzing Patient Data - 1

* Explain what a library is, and what libraries are used for.
* Load a Python library and use the things it contains.
* Read tabular data from a file into a program.
* Assign values to variables.
* Select individual values and subsections from data.


## Code Reminders

~~~ {.python}
import numpy
numpy.loadtxt(fname=..., delimiter=...)

weight_kg = 5          weight_lb = 2.2 * weight_kg
print weight_kg

type(data)                data.shape

data[0, 0]                 data[0:1, 0:1]
data[0:10:2, 1]         data[:3, 36:]
~~~


## Analyzing Patient Data - 2

* Perform operations on arrays of data.
* Display simple graphs.


## Code Reminders

~~~ {.python}
data.mean()    data.std()    data.mean(axis=0)

%matplotlib inline
from matplotlib import pyplot
pyplot.imshow(data)         pyplot.show()
pyplot.plot(ave_inflammation)

import matplotlib.pyplot as plt
plt.subplot(1, 3, 1)
plt.ylabel('average')       plt.show()
~~~


## Exercise

Create a single plot showing:

1. the mean for each day
2. the mean + 1 standard deviation for each day
3. the mean - 1 standard deviation for each day


## Creating Functions - 1

* Define a function that takes parameters.
* Return a value from a function.
* Test and debug a function.


## Code Reminders

~~~ {.python}
def fahr_to_kelvin(temp):
     return ((temp - 32) * (5/9)) + 273.15

from __future__ import division

def fahr_to_celsius(temp):
    temp_k = fahr_to_kelvin(temp)
    result = kelvin_to_celsius(temp_k)
    return result
~~~


## Creating Functions - 2

* Explain the scope of a variable and the idea of encapsulation.

![Python Call Stack](fig/python-call-stack-05.svg)


## Creating Functions - 3

* Test and document a function.
* Explain why we should divide programs into small, single-purpose functions.


## Code Reminders

~~~ {.python}
def centre(data, desired):
       return (data - data.mean()) + desired

z = numpy.zeros((2, 2))
print centre(z, 3)
print data.std() - centred.std()

def centre(data, desired):
       """Return a new array containing the
       original data centered around the desired
       value."""
~~~


##  Exercise

Write a function called `analyze` that takes a filename as a parameter and displays the three graphs produced in the previous lesson, i.e., `analyze('inflammation-01.csv')` should produce the graphs already shown, while `analyze('inflammation-02.csv')` should produce corresponding graphs for the second data set. Be sure to give your function a docstring.

Hint: a function can just "do" something.  It doesn't necessarily need to return anything.

## Creating Functions - 4

* Set default values for function parameters.


## Code Reminders

~~~ {.python}
def center(data, desired=0):

def display(a=1, b=2, c=3):
       print 'a:', a, 'b:', b, 'c:', c

print 'no parameters:', display()
print 'one parameter:', display(55)
print 'two parameters:', display(55, c=66)

help(numpy.loadtxt)
~~~


## Analyzing Multiple Data Sets - 1

You should have a working function `analyze`.
If not, its at the top of [http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/03-loop.ipynb](http://nbviewer.ipython.org/github/douglatornell/python-inflammation-2015-04-30-sfu/blob/gh-pages/03-loop.ipynb)

* Explain what a for loop does.
* Correctly write for loops to repeat simple calculations.


## Code Reminders

~~~ {.python}
def print_characters(element):
       print element[0]
       print element[1]
       print element[2]

print_characters('tin')
print_characters('hg')

def print_characters(element):
      for char in element:
           print char
~~~


## Analyzing Multiple Data Sets - 2

* Trace changes to a loop variable as the loop runs.
* Trace changes to other variables as they are updated by a for loop.


## Code Reminders

~~~ {.python}
length = 0
for vowel in 'aeiou':
    length = length + 1
print 'There are', length, 'vowels'

len('aeiou')

letter = 'z'
for letter in 'abc':
    print letter
print 'after the loop, letter is', letter
~~~


## Analyzing Multiple Data Sets - 3

* Explain what a list is.
* Create and index lists of simple values.


## Code Reminders

~~~ {.python}
odds = [1, 3, 5, 7]
odds[0], odds[-1]
for number in odds:

names = ['Newton', 'Darwig', 'Turing']
names[1] = 'Darwin'

name = 'Darwig'
name[5] = 'n'

odds.append[9]
del odds[0]
odds.reverse()
~~~


## Exercise

Write a function called `total` that calculates the sum of the values in a list.

(Python has a built-in function called `sum` that does this for you.
Please don't use it for this exercise.)


## Analyzing Multiple Data Sets - 4

* Use a library function to get a list of filenames that match a simple wildcard pattern.
* Use a for loop to process multiple files.


## Code Reminders

~~~ {.python}
import glob
print glob.glob('*.ipynb')

filenames = glob.glob('*.csv')
filenames = filenames[0:3]
for f in filenames:
      print f
      analyze(f)
~~~


## Conditionals -- Making Choices

* Write conditional statements including `if`, `elif`, and `else` branches.
* Correctly evaluate expressions containing `and` and `or`.
* Correctly write and interpret code containing nested loops and conditionals.


## Code Reminders

~~~ {.python}
numpy.empty()
numpy.empty_like()

+=, -=, *=, /=

enumerate()

if ... elif ... else

==, !=, <, <=, >, >=
and, or, not
~~~


## Code Reminders

* Non-printing characters; e.g. `\n`
* Line continuations in code
