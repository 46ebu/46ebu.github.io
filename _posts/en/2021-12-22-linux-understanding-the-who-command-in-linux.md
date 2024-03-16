---
title: "[linux] Understanding the 'who' command in Linux"
author: 46ebu
date: 2021-12-22 06:23:20 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-understanding-the-who-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
In the Linux operating system, the 'who' command is used to display information about users who are currently logged in to the system. It provides details such as the username, terminal, login time, and remote host from which the user is logged in. Understanding how to use the 'who' command can be helpful for monitoring user activity and managing system resources efficiently.

### Syntax
The basic syntax of the 'who' command is as follows:
```
who [OPTION]... [FILE]...
```
Here, OPTION is used to specify any additional options for the command, and FILE is the name of a file containing an alternate list of users. If no options are specified, the 'who' command will display information about all users currently logged in.

### Examples
1. To display a list of all users currently logged in:
```
who
```
This command will show the username, terminal, login time, and remote host for each user currently logged in to the system.

2. To display only the usernames of users currently logged in:
```
who -q
```
The '-q' option is used to show only the usernames of users currently logged in, without any additional information.

3. To display information about the last user who logged in:
```
who -u
```
The '-u' option shows information about the last user who logged in, including the username, terminal, login time, and duration of login.

### Applicable Versions
The 'who' command is available in most Unix-like operating systems, including Linux. It is a standard utility found in the GNU Core Utilities package, which is typically included with most Linux distributions. The examples provided in this blog post should work on most modern versions of Linux without any issues.

### Conclusion
In conclusion, the 'who' command in Linux is a useful tool for monitoring user activity and managing system resources. By understanding how to use this command effectively, system administrators can keep track of who is currently logged in, identify any suspicious activity, and take appropriate action if necessary. By incorporating the 'who' command into their regular system monitoring routine, administrators can maintain a secure and efficient computing environment.