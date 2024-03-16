---
title: "[Python] Introduction to Flask for Web Development"
author: 46ebu
date: 2024-03-15 22:01:49 +0900
categories: [python]
tags: [python]
render_with_liquid: false
---

![Intro](/assets/img/post/python.png)
## What is Flask?

Flask is a lightweight WSGI web application framework written in Python. It is designed to be simple and easy to use, yet powerful enough to handle complex web development tasks. Flask is known for its flexibility, making it a popular choice among developers for building web applications.

## Getting Started with Flask

To start using Flask for web development, you first need to install it using pip. You can create a virtual environment and install Flask by running the following commands in your terminal:

```python
pip install flask
```

Once Flask is installed, you can create a new Flask application by creating a new Python file and importing the `Flask` class from the `flask` module. You then create an instance of the `Flask` class, passing in the name of your module or package as the constructor argument.

```python
from flask import Flask

app = Flask(__name__)
```

## Creating Routes in Flask

In Flask, a route is a URL pattern that the application uses to match against incoming requests and trigger the associated view function. You can create routes in Flask by using the `route` decorator, which maps a URL to a view function. Here's an example of defining a simple route in Flask:

```python
@app.route('/')
def index():
    return 'Hello, World!'
```

In the code snippet above, we define a route for the root URL (`/`) that calls the `index` function and returns a simple string response.

## Running a Flask Application

To run a Flask application, you can simply use the `run` method on your `app` instance. By default, the Flask development server runs on `http://127.0.0.1:5000/`, allowing you to access your application in a web browser. You can start your Flask application by running the following code:

```python
if __name__ == '__main__':
    app.run()
```

## Conclusion

In conclusion, Flask is a powerful Python web framework that offers simplicity and flexibility for web development. By following the steps outlined in this blog post, you can get started with Flask and begin building web applications in Python. Flask is compatible with Python versions 2.7 and 3.5 or higher, making it a versatile choice for developers. Start exploring Flask today and unlock the potential of web development with Python!