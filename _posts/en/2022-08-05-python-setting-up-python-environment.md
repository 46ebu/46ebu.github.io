---
title: "[python] Setting Up Python Environment"
author: 46ebu
date: 2022-08-05 10:21:18 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-setting-up-python-environment
---

![Intro](/assets/img/post/python.png)
### Installing Python

Setting up a Python environment is the first step for anyone looking to start coding in Python. To do this, you need to install Python on your machine. The latest stable version of Python can be downloaded from the official Python website. Once you have downloaded the installer, run it and follow the installation instructions to complete the setup.

```python
print("Hello, Python!")
```

### Checking Python Version

After the installation is complete, you can check the Python version installed on your machine using the terminal or command prompt. Simply type `python --version` or `python -V`, and the version number will be displayed. It is recommended to always use the latest stable version of Python to take advantage of the latest features and updates.

```python
import sys
print(sys.version)
```

### Creating a Virtual Environment

A virtual environment is a self-contained directory that contains a Python installation for a particular version of Python, plus a number of additional packages. To create a virtual environment, you can use the built-in `venv` module in Python. Navigate to the directory where you want to create the virtual environment and run the following command:

```python
python -m venv myenv
```

### Activating the Virtual Environment

Once the virtual environment is created, you need to activate it before you can start using it. On Windows, you can activate the virtual environment by running the `activate` script in the `Scripts` directory inside the virtual environment:

```python
myenv\Scripts\activate
```

On macOS and Linux, you can activate the virtual environment by running the `activate` script in the `bin` directory inside the virtual environment:

```python
source myenv/bin/activate
```

### Installing Packages using pip

`pip` is the package installer for Python. Once your virtual environment is activated, you can use `pip` to install packages from the Python Package Index (PyPI). For example, to install the `requests` package, you can run:

```python
pip install requests
```

### Creating a Requirement.txt File

To keep track of the packages used in your project, you can create a `requirements.txt` file that lists all the dependencies. To generate the file, you can use the following command:

```python
pip freeze > requirements.txt
```

### Summary

Setting up a Python environment involves installing Python, creating a virtual environment, activating the virtual environment, and installing packages using `pip`. By following these steps, you can ensure that your Python projects are isolated and organized, making it easier to manage dependencies and collaborate with others.