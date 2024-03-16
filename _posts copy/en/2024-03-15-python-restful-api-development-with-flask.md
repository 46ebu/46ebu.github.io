---
title: "[Python] RESTful API Development with Flask"
author: 46ebu
date: 2024-03-15 22:08:21 +0900
categories: [python]
tags: [python]
render_with_liquid: false
---

![Intro](/assets/img/post/python.png)
### Introduction

Flask is a popular Python web framework that is widely used for developing web applications and APIs. When it comes to building RESTful APIs, Flask provides a simple and flexible way to create APIs that adhere to the REST architectural style. In this blog post, we will explore how to develop RESTful APIs with Flask in Python.

### Setting up Flask

To get started with Flask, you first need to install the Flask package using pip. You can do this by running the following command in your terminal:

```python
pip install Flask
```

Once Flask is installed, you can create a new Flask application by creating a new Python file and importing the Flask module:

```python
from flask import Flask

app = Flask(__name__)
```

### Creating API Endpoints

In Flask, API endpoints are represented by functions that are decorated with route decorators. For example, to create a simple endpoint that returns a JSON response, you can define a function like this:

```python
from flask import jsonify

@app.route('/hello', methods=['GET'])
def hello():
    return jsonify({'message': 'Hello, World!'})
```

### Handling Request Data

Flask provides built-in support for handling request data, such as query parameters or JSON payloads. You can access request data using the `request` object. Here's an example of how to handle a POST request and extract data from the request body:

```python
from flask import request

@app.route('/user', methods=['POST'])
def create_user():
    data = request.json
    name = data.get('name')
    email = data.get('email')
    # Perform user creation logic here
    return jsonify({'message': 'User created successfully'})
```

### Running the Flask Application

To run your Flask application, you can use the `run` method of the Flask app object. By default, the Flask development server runs on port 5000. Here's how you can run your Flask application:

```python
if __name__ == '__main__':
    app.run()
```

### Conclusion

In this blog post, we have covered the basics of developing RESTful APIs with Flask in Python. Flask provides a powerful and flexible framework for building APIs that adhere to the principles of REST. By following the examples and guidelines provided in this post, you can create robust and scalable APIs using Flask. Happy coding!