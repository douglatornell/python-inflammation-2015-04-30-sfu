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


## Creating Functions Part 2

* Explain the scope of a variable and the idea of encapsulation.

![Python Call Stack](fig/python-call-stack-05.png)
