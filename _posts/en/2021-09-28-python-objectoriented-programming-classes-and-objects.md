---
title: "[python] Object-Oriented Programming: Classes and Objects"
author: 46ebu
date: 2021-09-28 02:26:21 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-objectoriented-programming-classes-and-objects
---

![Intro](/assets/img/post/python.png)
### Introduction to Object-Oriented Programming in Python

Object-Oriented Programming (OOP) is a programming paradigm that revolves around the concept of "objects," which can contain data in the form of attributes and code in the form of methods. Classes are blueprints for creating objects in OOP languages like Python. 

In Python, everything is an object, and classes are no exception. To define a class in Python, you use the `class` keyword followed by the class name and a colon. 

### Syntax of Defining a Class 

Here is an example of a simple class in Python:

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
```

In this example, we define a class called `Person` with an `__init__` method that sets the `name` and `age` attributes of a `Person` object. The `self` parameter is a reference to the current instance of the class.

### Creating Objects from a Class

In OOP, objects are instances of classes. To create an object from a class in Python, you simply call the class like a function. 

Here is an example of creating an object from the `Person` class:

```python
person1 = Person("Alice", 30)
print(person1.name) # Output: Alice
print(person1.age) # Output: 30
```

In this example, we create a `Person` object named `person1` with the name "Alice" and age 30. We then access the `name` and `age` attributes of the `person1` object using dot notation.

### Class Inheritance and Polymorphism

In Python, classes can inherit from other classes, allowing for code reuse and the creation of more specialized classes. 

Here is an example of class inheritance in Python:

```python
class Student(Person):
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id

student1 = Student("Bob", 25, "12345")
print(student1.name) # Output: Bob
print(student1.age) # Output: 25
print(student1.student_id) # Output: 12345
```

In this example, the `Student` class inherits from the `Person` class. The `super()` function is used to call the `__init__` method of the `Person` class.

### Conclusion 

Classes and objects are fundamental to object-oriented programming in Python. By defining classes, creating objects, and using inheritance, you can build complex and reusable code that models real-world entities effectively. Python's OOP capabilities make it a powerful and versatile language for developing software applications. 

Python versions 3.x fully support OOP concepts and syntax, making it an excellent choice for developers looking to leverage the benefits of OOP in their projects.