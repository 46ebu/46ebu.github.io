---
title: "[python] Control Flow: If Statements and Loops"
author: 46ebu
date: 2021-03-14 17:37:14 
categories: [python]
tags: [python]
render_with_liquid: false
lang: en
permalink: /python-control-flow-if-statements-and-loops
---

![Intro](/assets/img/post/python.png)
### If Statements and Loops in Python

Control flow structures like if statements and loops are essential in programming to make decisions and repeat certain actions. In Python, these structures are used to control the flow of the program based on certain conditions. Let's dive into the details of if statements and loops in Python.

### If Statements

If statements are used to execute a block of code only if a certain condition is true. The syntax for an if statement in Python is as follows:

```python
if condition:
    # code to be executed if the condition is true
```

The condition can be any expression that evaluates to a boolean value (True or False). If the condition is true, the indented block of code following the if statement is executed. Otherwise, the code is skipped. 

Let's look at an example:

```python
x = 10

if x > 5:
    print("x is greater than 5")
```

In this example, the condition `x > 5` is true since the value of x is 10. Therefore, the code inside the if statement is executed and "x is greater than 5" is printed.

### Loops

Loops are used to repeat a block of code multiple times. There are two main types of loops in Python: for loops and while loops.

#### For Loops

For loops are used when you know the number of iterations in advance. The syntax for a for loop in Python is as follows:

```python
for i in range(n):
    # code to be repeated n times
```

In this syntax, `range(n)` generates a sequence of numbers from 0 to n-1. The variable `i` takes the value of each number in the sequence in each iteration of the loop. 

Here's an example of a for loop:

```python
for i in range(5):
    print(i)
```

This loop will print numbers from 0 to 4, as the range function generates a sequence of numbers from 0 to 4.

#### While Loops

While loops are used when you don't know the number of iterations in advance but have a condition that needs to be met for the loop to continue. The syntax for a while loop in Python is as follows:

```python
while condition:
    # code to be repeated as long as the condition is true
```

In this syntax, the code inside the while loop is executed repeatedly as long as the condition is true. If the condition becomes false, the loop terminates.

Here's an example of a while loop:

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

In this example, the loop will print numbers from 0 to 4, as long as the condition `x < 5` is true. The value of x is incremented by 1 in each iteration.

### Conclusion

If statements and loops are fundamental control flow structures in Python that allow you to make decisions and repeat actions. By using if statements, for loops, and while loops effectively, you can create more powerful and flexible programs. Make sure to practice and experiment with different conditions and iterations to master control flow in Python.