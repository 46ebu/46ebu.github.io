---
title: "[python] json read/write/update method (code example and explanation)"
author: 46ebu
date: 2024-04-12 15:35:00 +0000
categories: [python]
tags: [python]
render_with_liquid: false
---

![Intro](/assets/img/post/python.png)
### Introduction
JSON (JavaScript Object Notation) is a lightweight data interchange format commonly used for storing and transmitting data on the web. In Python, the `json` module provides methods for reading, writing, and updating JSON data. In this blog post, we will explore how to use these methods with code examples and explanations.

### Reading JSON Data
To read JSON data in Python, you can use the `json.load()` method to deserialize a JSON object from a file-like object. Here is an example code snippet:

```python
import json

# Open and read a JSON file
with open('data.json', 'r') as file:
    data = json.load(file)

print(data)
```

In this example, we open a JSON file named `data.json` and load its contents into the `data` variable using the `json.load()` method. The `print(data)` statement then outputs the deserialized JSON data.

### Writing JSON Data
To write JSON data in Python, you can use the `json.dump()` method to serialize a Python object into a JSON formatted stream. Here is an example code snippet:

```python
import json

# Python object to be serialized
data = {
    "name": "John Doe",
    "age": 30,
    "city": "New York"
}

# Write the object to a JSON file
with open('output.json', 'w') as file:
    json.dump(data, file, indent=4)

print("Data written successfully")
```

In this example, we create a Python dictionary `data`, which represents the JSON object to be serialized. We then use the `json.dump()` method to write the object to a file named `output.json` with an indentation of 4 for better readability.

### Updating JSON Data
To update JSON data in Python, you can read the existing JSON file, modify the data, and then write it back to the file. Here is an example code snippet demonstrating this process:

```python
import json

# Read and update JSON data
with open('data.json', 'r') as file:
    data = json.load(file)
    
    data['age'] = 31

# Write updated data back to the JSON file
with open('data.json', 'w') as file:
    json.dump(data, file, indent=4)

print("Data updated successfully")
```

In this example, we read the JSON data from `data.json`, update the value of the `age` key in the JSON object, and then write the updated data back to the same file.

### Conclusion
In this blog post, we have explored the JSON read, write, and update methods in Python using the `json` module. By utilizing these methods, you can easily work with JSON data in your Python programs. These methods provide a convenient way to interact with JSON data, making it a valuable tool for handling data interchange.