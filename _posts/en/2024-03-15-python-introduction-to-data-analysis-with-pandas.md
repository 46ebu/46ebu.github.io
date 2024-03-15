---
title: "[python] Introduction to Data Analysis with Pandas"
author: 46ebu
date: 2024-03-15 22:10:36 +0900
categories: [python]
tags: [python]
render_with_liquid: false
---

![Intro](/assets/img/post/python.png)
### What is Pandas?

Pandas is one of the most popular Python libraries used for data manipulation and analysis. It provides data structures like Series and DataFrame that are efficient and easy to use for working with structured data. Pandas is built on top of NumPy, another popular library in Python for numerical computing, and provides tools for reading and writing data, cleaning and transforming data, and analyzing data efficiently.

### Installing Pandas

Before you start using Pandas, you need to install it on your system. You can use pip, the Python package installer, to install Pandas. Simply run the following command in your terminal:

```python
pip install pandas
```

### Creating a DataFrame

One of the key data structures in Pandas is the DataFrame. You can think of a DataFrame as a table with rows and columns, similar to a spreadsheet or a SQL table. You can create a DataFrame from a dictionary, a list of dictionaries, or from external data sources like CSV files.

```python
import pandas as pd

data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35],
        'City': ['New York', 'San Francisco', 'Los Angeles']}

df = pd.DataFrame(data)
print(df)
```

### Reading and Writing Data

Pandas provides tools for reading and writing data from/to various file formats like CSV, Excel, SQL databases, and more. You can use functions like `read_csv()` and `to_csv()` to read and write data from/to CSV files:

```python
# Read data from a CSV file
df = pd.read_csv('data.csv')

# Write data to a CSV file
df.to_csv('output.csv', index=False)
```

### Indexing and Selection

You can select and manipulate data in a DataFrame using various indexing methods. You can use column labels, row indices, or boolean arrays to select subsets of data. For example, you can select data based on certain conditions like filtering rows where the age is greater than 30:

```python
# Select data where the age is greater than 30
filtered_df = df[df['Age'] > 30]
print(filtered_df)
```

### Applicable Python Versions

Pandas is compatible with Python 3.6 and above. It is recommended to use the latest version of Python and Pandas to leverage the latest features and improvements.

In conclusion, Pandas is a powerful library in Python for data analysis and manipulation. By using Pandas, you can efficiently clean, transform, and analyze data to derive valuable insights. It is widely used in various fields like data science, finance, and research. The examples provided above give a brief overview of how to get started with Pandas in Python.