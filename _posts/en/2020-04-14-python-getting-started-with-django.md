---
title: "[python] Getting Started with Django"
author: 46ebu
date: 2020-04-14 19:59:54 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-getting-started-with-django
---

![Intro](/assets/img/post/python.png)
### Introduction to Django
Django is a popular high-level web framework written in Python that encourages rapid development and clean, pragmatic design. It follows the Model-View-Template (MVT) pattern, similar to Model-View-Controller (MVC), where the model represents the data structure, the view represents the user interface, and the template represents the presentation layer. 

### Installation
To get started with Django, you need to have Python installed on your system. You can install Django using pip, Python's package installer, by running:

```
pip install Django
```

### Creating a Django Project
To create a new Django project, use the following command:

```
django-admin startproject project_name
```

This will create a directory with the project's structure and files. The main project directory contains settings.py, urls.py, and wsgi.py files, while the inner project directory contains the manage.py file.

### Creating a Django App
Inside the Django project directory, you can create a new app using the following command:

```
python manage.py startapp app_name
```

This will create a new directory for the app with the necessary files for models, views, and templates.

### Running the Development Server
To run the development server and test your Django project, use the following command:

```
python manage.py runserver
```

This will start the development server on http://127.0.0.1:8000/. You can access your project by navigating to this URL in your web browser.

### Django Version Compatibility
It is important to note that Django has different versions, and some features may vary based on the version you are using. Make sure to check the Django documentation for the specific version you are working with to ensure compatibility and proper usage of features.

### Conclusion
Getting started with Django can be a rewarding experience for developers looking to build web applications quickly and efficiently. By following the steps outlined in this post, you can create a Django project, build apps, and run the development server to test your application. Django's rich ecosystem of libraries and tools makes it a popular choice for web development projects in Python.