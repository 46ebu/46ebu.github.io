---
title: "[python] Introduction to Flask for Web Development"
author: 46ebu
date: 2021-06-27 12:16:54 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-introduction-to-flask-for-web-development
---

![Intro](/assets/img/post/python.png)
### What is Flask?
Flask is a micro web framework written in Python. It is lightweight, easy to use, and customizable, making it a popular choice for web development projects. Flask provides tools to help build web applications quickly and efficiently, with its simplicity and flexibility allowing developers to create a wide variety of web applications.

### Setting up Flask
To start using Flask, you first need to install it. You can do this using pip, the Python package installer. Simply run `pip install Flask` in your terminal. Once Flask is installed, you can start building your web application by creating a new Python file and importing the Flask module.

### Creating a basic Flask application
Let's create a simple "Hello, World!" application in Flask:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run()
```

In this code snippet, we import the Flask module, create a new Flask application instance, define a route for the root URL ('/'), and create a function to handle requests to that route.

### Running the Flask application
To run your Flask application, save the code in a file (e.g., `app.py`) and execute it using the Python interpreter. You should see a message indicating that the app is running on a local server. You can then open a web browser and navigate to `http://127.0.0.1:5000` to see your "Hello, World!" message.

### Conclusion
Flask is a powerful web development framework that simplifies the process of building web applications in Python. Its minimalist design and extensive documentation make it easy for beginners to get started, while its flexibility and scalability appeal to more experienced developers. Whether you're creating a simple personal website or a complex web application, Flask provides the tools you need to bring your ideas to life in the online world.