---
title: "Working with External Libraries in Python"
author: 46ebu
date: 2020-01-13 10:47:50 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /working-with-external-libraries-in-python
---

![Intro](/assets/img/post/python.png)
### Introduction
Working with external libraries in Python allows developers to leverage existing code and functionalities to enhance their own projects. These libraries provide pre-written code that can be easily imported and used in Python scripts, making development faster and more efficient.

### Importing External Libraries
To use an external library in a Python script, you first need to import it using the `import` keyword followed by the library name. For example, to import the popular NumPy library for numerical computations, you would use:
```python
import numpy
```
You can also import specific modules or functions from a library using the `from` keyword. For example, to import just the `array` function from NumPy, you would use:
```python
from numpy import array
```

### Installing External Libraries
Before you can use an external library in your Python script, you need to install it using a package manager like `pip`. You can install a library by running the following command in your terminal:
```bash
pip install numpy
```
This command will download and install the NumPy library and all its dependencies on your machine.

### Using External Libraries
Once you have imported and installed an external library, you can start using its functions and classes in your Python script. For example, you can create a NumPy array and perform operations on it like this:
```python
import numpy as np

arr = np.array([1, 2, 3, 4, 5])
print(arr)
```
In this example, we import NumPy as `np` and create a NumPy array `arr` using the `array` function. We then print the array to the console.

### Python Versions
Working with external libraries in Python is supported in both Python 2 and Python 3. However, it is recommended to use Python 3 as Python 2 is no longer maintained and will not receive updates or bug fixes.

### Conclusion
In conclusion, working with external libraries in Python is essential for developers looking to streamline their development process and leverage existing code. By following the steps outlined in this post, you can easily import, install, and use external libraries in your Python projects.