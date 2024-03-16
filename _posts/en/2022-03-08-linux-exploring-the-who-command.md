---
title: "[linux] Exploring the 'who' command"
author: 46ebu
date: 2022-03-08 11:57:29 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-exploring-the-who-command
---

![Intro](/assets/img/post/linux.png)
### Introduction 
In the world of Linux, the 'who' command is a handy tool used to display information about currently logged-in users on the system. It provides details such as username, terminal, login time, and more. Let's dive deeper into how this command can be utilized effectively.

### Syntax
The basic syntax of the 'who' command is quite simple:
```
who [OPTION]... [FILE]...
```
Here, the OPTIONS can be used to customize the output according to your requirements. You can specify a file as an argument to display the users logged in from a particular file.

### Example codes
1. To display a basic list of currently logged-in users:
```
who
```
This will show the username, terminal, and login time for each user.

2. To display detailed information about the users:
```
who -a
```
This will provide additional details such as system boot time, idle time, and process ID.

3. To display the hostname along with user information:
```
who -H
```
This will show the hostname in the output along with other details.

### Applicable versions
The 'who' command is available on most Unix-based systems, including Linux distributions. It is a standard command and comes pre-installed on these systems. You can use it on popular distributions like Ubuntu, CentOS, Fedora, and more.

### Conclusion
In conclusion, the 'who' command is a useful tool for system administrators to monitor user activity on a Linux system. By understanding its syntax and options, you can gather relevant information about logged-in users efficiently. Experiment with different options to customize the output according to your needs. Mastering this command will help you keep track of user sessions and manage your system effectively.