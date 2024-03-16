---
title: "[linux] The 'who' Command in Linux"
author: 46ebu
date: 2022-08-08 15:57:04 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-the-who-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction to 'who' Command 
The 'who' command in Linux is a simple utility that displays information about users who are currently logged into the system. It provides details such as the username, terminal name, login time, and IP address. This command is commonly used by system administrators to monitor user activity on a system.

### Syntax of 'who' Command
The basic syntax of the 'who' command is as follows:
```
who [OPTION]... [FILE]...
```
Some commonly used options with the 'who' command are:
- `-b`: Display the time when the system was last booted
- `-q`: Display the number of logged-in users
- `-H`: Display the column headers
- `-u`: Show the idle time for each logged-in user

### Examples of 'who' Command
1. Displaying currently logged-in users:
```
who
```
This command will show a list of all users who are currently logged into the system along with additional details such as terminal, login time, and IP address.

2. Showing the number of logged-in users:
```
who -q
```
By using the `-q` option, you can quickly see the total number of users currently logged into the system.

3. Displaying the time of the last system boot:
```
who -b
```
This command will show you the timestamp of when the system was last booted.

### Versions and Compatibility
The 'who' command is a standard utility found in most Unix-like operating systems, including Linux. It is available on all major Linux distributions such as Ubuntu, CentOS, and Fedora. The command may have minor syntax variations across different versions, but the basic functionality remains the same.

In conclusion, the 'who' command in Linux is a handy tool for monitoring user activity on a system. Whether you need to see a list of currently logged-in users, check the number of users, or view the time of the last system boot, the 'who' command has got you covered. With its simple syntax and useful options, it is an essential utility for system administrators and power users alike.