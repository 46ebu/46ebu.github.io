---
title: "[python] Object-Oriented Programming: Classes and Objects"
author: 46ebu
date: 2023-10-18 09:11:42 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-objectoriented-programming-classes-and-objects
---

![Intro](/assets/img/post/python.png)
### Introduction
Object-oriented programming (OOP) is a programming paradigm that revolves around the concept of "objects," which are instances of classes. In Python, classes and objects play a crucial role in building scalable and maintainable code. Let's delve into the fundamentals of classes and objects in Python.

### Classes in Python
A class is a blueprint for creating objects, defining the attributes (variables) and methods (functions) that the objects will possess. In Python, classes are defined using the `class` keyword followed by the class name. It is convention to use CamelCase for class names. Here's an example class called `Car`:

```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
    
    def display_info(self):
        print(f"The car is a {self.make} {self.model}")
```

### Objects in Python
Objects are instances of classes, which means they are created based on the structure provided by the class. You can create an object of a class by calling the class name followed by parentheses. Here's how you can create an object of the `Car` class:

```python
my_car = Car("Toyota", "Camry")
my_car.display_info()
```

### Instances and Attributes
Each object created from a class is considered an instance of that class. Objects have attributes that are specific to them. In the `Car` class example above, `make` and `model` are attributes of the object `my_car`. You can access these attributes using dot notation, like `my_car.make`.

### Methods in Classes
Methods in classes are functions that belong to the class and operate on the attributes of an object. In the `Car` class, `display_info` is a method that prints out the make and model of the car. Methods are defined within a class using the `def` keyword.

### Inheritance in Classes
Inheritance allows a class to inherit attributes and methods from another class. This promotes code reusability and enables the creation of a hierarchy of classes. In Python, you can create a class that inherits from another class by passing the parent class in parentheses after the class name. Here's an example:

```python
class ElectricCar(Car):
    def __init__(self, make, model, battery_size):
        super().__init__(make, model)
        self.battery_size = battery_size
    
    def display_info(self):
        print(f"The electric car is a {self.make} {self.model} with a {self.battery_size}-kWh battery")
```

### Conclusion
Classes and objects are essential components of object-oriented programming in Python. They provide a way to structure and organize code, making it easier to manage and understand. By creating classes and defining objects, you can build flexible and scalable applications that adhere to the principles of OOP. Experiment with creating your own classes and objects to explore the power of OOP in Python.