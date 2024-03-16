---
title: "[python] Database Interaction with Python"
author: 46ebu
date: 2020-06-18 10:13:01 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-database-interaction-with-python
---

![Intro](/assets/img/post/python.png)
### Introduction
Database interaction with Python is a common task in software development. Python provides various libraries and frameworks that allow developers to interact with databases easily. In this blog post, we will explore how to interact with databases using Python.

### Connecting to a Database
To interact with a database in Python, you first need to establish a connection to the database. This can be done using libraries such as `sqlite3` for SQLite, `psycopg2` for PostgreSQL, or `mysql-connector-python` for MySQL. 

```python
import sqlite3

# Connect to a database
conn = sqlite3.connect('example.db')
```

### Executing SQL Queries
Once you have established a connection to the database, you can execute SQL queries to interact with the data. The `cursor` object is used to execute SQL statements.

```python
# Create a cursor object
cursor = conn.cursor()

# Execute an SQL query
cursor.execute("SELECT * FROM users")

# Fetch all rows from the result query
rows = cursor.fetchall()

# Iterate over the rows
for row in rows:
    print(row)
```

### Committing Changes
After executing SQL queries that modify the database, you need to commit the changes to save them permanently.

```python
# Insert a new record into the database
cursor.execute("INSERT INTO users (name, age) VALUES ('Alice', 30)")

# Commit the changes
conn.commit()
```

### Closing the Connection
It is important to close the database connection when you are done interacting with the database to free up resources.

```python
# Close the cursor
cursor.close()

# Close the connection
conn.close()
```

### Conclusion
In this blog post, we have learned how to interact with a database using Python. We covered connecting to a database, executing SQL queries, committing changes, and closing the connection. By following these steps, you can effectively interact with various databases using Python. Keep in mind the specific syntax for the database library you are using and ensure compatibility with your Python version. 

Python provides a convenient and efficient way to interact with databases, making it a popular choice for database integration in software development projects. Whether you are working with SQLite, PostgreSQL, MySQL, or other databases, Python has the tools and libraries to make database interaction seamless and easy. Happy coding!