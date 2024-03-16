---
title: "Exploring the 'who' Command in Linux"
author: 46ebu
date: 2020-02-14 07:58:50 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /exploring-the-who-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
The 'who' command in Linux is a versatile tool used to display information about users who are currently logged in to the system. It provides details such as the username, terminal, login time, and more. This command is particularly useful for system administrators who need to monitor user activity on a server.

### Syntax
The basic syntax of the 'who' command is as follows:

```bash
who [OPTION]...
```

Some common options that can be used with the 'who' command include:
- `-H`: Display column headers.
- `-q`: Display only the number of users logged on.
- `-u`: Display idle time as well.

### Examples
1. To display a list of all users currently logged in, along with additional details, simply run:
```bash
who
```
This will output information such as username, terminal, login time, IP address, and more.

2. If you want to display only the usernames of users currently logged in, you can use the '-q' option:
```bash
who -q
```
This will show you a simple list of usernames, without any additional information.

3. To display detailed information about a specific user, you can specify the username as an argument:
```bash
who username
```
This will show you specific details about the user, including their terminal, login time, and more.

### Applicable Versions
The 'who' command is available in most Linux distributions, including Ubuntu, CentOS, and Fedora. It is a standard utility that comes pre-installed with the operating system, so you can start using it right away without any additional setup.

In conclusion, the 'who' command in Linux is a powerful tool for monitoring user activity on a system. Whether you need to keep track of who is currently logged in or obtain detailed information about a specific user, this command has you covered. By understanding its syntax and options, you can leverage the 'who' command to effectively manage user sessions on your Linux system.