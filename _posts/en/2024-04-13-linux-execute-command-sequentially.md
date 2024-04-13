---
title: "[linux] execute command sequentially"
author: 46ebu
date: 2024-04-13 01:50:40 +0000
categories: [linux]
tags: [linux]
render_with_liquid: false
---

![Intro](/assets/img/post/linux.png)
### Introduction
In Linux, the ability to execute commands sequentially allows users to perform a series of tasks in a specific order without the need for manual intervention. By chaining commands together using certain operators or constructs, users can automate processes, save time, and increase efficiency in their workflow.

### Syntax for Sequential Execution
In Linux, there are several ways to execute commands sequentially. The most common methods include using the semicolon (;), double ampersand (&&), or double vertical bar (||) operators. These operators dictate the behavior of the commands that follow them based on the success or failure of the preceding command.

- Using a semicolon (;) between commands will execute each command independently of the others, regardless of whether the previous command succeeded or failed.
- Using double ampersands (&&) between commands will execute the subsequent command only if the previous command succeeded.
- Using double vertical bars (||) between commands will execute the subsequent command only if the previous command failed.

### Example Codes and Output
Let's explore these concepts with some examples:

1. Sequential execution using semicolons:
```bash
echo "Hello, " ; echo "world!"
```
Output:
```
Hello,
world!
```

2. Sequential execution using double ampersands:
```bash
mkdir test && cd test && touch file.txt
```
Output:
```
(file.txt will be created inside the 'test' directory only if the 'test' directory is successfully created first)

3. Sequential execution using double vertical bars:
```bash
ls non_existent_directory || echo "Directory does not exist"
```
Output:
```
Directory does not exist
```

### Applicable Versions
Sequential execution of commands using operators like semicolons, double ampersands, and double vertical bars is supported in most, if not all, versions of Linux distributions. Users can leverage these constructs in their shell scripts or command-line interface to streamline their workflow and automate tasks effectively.

In conclusion, understanding and utilizing sequential execution of commands in Linux can greatly enhance productivity and efficiency for users. By mastering these operators and constructs, users can create complex workflows and automate repetitive tasks with ease.