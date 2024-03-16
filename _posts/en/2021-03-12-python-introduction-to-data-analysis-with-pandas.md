---
title: "[python] Introduction to Data Analysis with Pandas"
author: 46ebu
date: 2021-03-12 08:15:10 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-introduction-to-data-analysis-with-pandas
---

![Intro](/assets/img/post/python.png)
### What is Pandas?
Pandas is a popular Python library used for data manipulation and analysis. It provides data structures like DataFrames and Series that make working with tabular data much easier. Pandas is built on top of NumPy, which makes it fast and efficient for data processing tasks.

### Installing Pandas
To install Pandas, you can use pip, the Python package manager. Simply run `pip install pandas` in your command line to install the library. Pandas is compatible with Python 3.6 or higher.

### Getting Started with DataFrames
One of the key data structures in Pandas is the DataFrame, which is a two-dimensional labeled data structure with columns of potentially different types. You can create a DataFrame from a dictionary, a list of lists, or by reading data from a file.

```python
import pandas as pd

# Creating a DataFrame from a dictionary
data = {'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35]}
df = pd.DataFrame(data)

print(df)
```

### Basic Data Analysis with Pandas
Pandas provides a wide range of functions for data analysis tasks such as filtering, grouping, and aggregating data. You can easily select rows and columns using labels or indices, apply functions to columns, and merge DataFrames.

```python
# Filtering data
filtered_df = df[df['Age'] > 30]

# Grouping and aggregating data
grouped_df = df.groupby('Age').size()

# Merging DataFrames
data2 = {'Name': ['David', 'Eve'],
         'Age': [40, 45]}
df2 = pd.DataFrame(data2)

merged_df = pd.concat([df, df2])
```

### Conclusion
In this post, we've introduced the basics of data analysis with Pandas in Python. Pandas is a powerful library that simplifies working with tabular data and provides a range of functions for data manipulation and analysis. By mastering Pandas, you can become more efficient at handling and analyzing data in your Python projects.