---
title: "[python] Unit Testing in Python with pytest"
author: 46ebu
date: 2020-03-22 18:21:02 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-unit-testing-in-python-with-pytest
---

![Intro](/assets/img/post/python.png)
### Introduction
Unit testing is an essential practice in software development to ensure that individual units or components of a program work as expected. In Python, pytest is a popular testing framework that makes writing and running tests easier and more efficient.

### Setting up pytest
To start using pytest for unit testing in Python, you first need to install the pytest package using pip:
```
pip install pytest
```
Once pytest is installed, you can create test files with functions that start with `test_` to indicate that they are test functions.

### Writing test cases
In pytest, you can use assertions to check if a given condition is true. For example, you can write a test case to check if a function returns the expected output:
```python
def add(x, y):
    return x + y

def test_add():
    assert add(1, 2) == 3
```
In this example, the `test_add` function uses the `assert` statement to verify that the `add` function correctly adds two numbers. If the assertion fails, pytest will raise an AssertionError and provide details about the failure.

### Running tests
To run your test cases with pytest, you can simply use the command:
```
pytest
```
Pytest will automatically discover your test functions in files that start with `test_` or end with `_test.py` and execute them. You will see a report of the test results, including any failures or errors.

### Parameterized tests
Pytest allows you to run the same test with multiple inputs using parameterized tests. You can use the `@pytest.mark.parametrize` decorator to specify the test inputs and expected outputs:
```python
import pytest

def multiply(x, y):
    return x * y

@pytest.mark.parametrize("x, y, expected", [(2, 3, 6), (4, 5, 20)])
def test_multiply(x, y, expected):
    assert multiply(x, y) == expected
```
In this example, the `test_multiply` function is parameterized with different inputs and expected outputs, allowing you to test the `multiply` function with multiple test cases in a single test function.

### Conclusion
Unit testing with pytest in Python is a powerful and flexible way to ensure the correctness of your code. By writing test cases, running tests, and using features like assertions and parameterized tests, you can improve the quality and reliability of your software.pytest is supported in Python 2.7, 3.5, 3.6, 3.7, and 3.8, making it compatible with a wide range of Python versions. Start incorporating unit testing into your Python development workflow with pytest to build robust and error-free applications.