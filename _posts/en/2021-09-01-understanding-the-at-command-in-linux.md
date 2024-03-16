---
title: "Understanding the 'at' Command in Linux"
author: 46ebu
date: 2021-09-01 10:53:38 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /understanding-the-at-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
In Linux, the 'at' command is a tool that allows users to schedule tasks to be run at a specified time in the future. This can be useful for automating tasks or executing scripts at specific times without needing to be actively running. The 'at' command is a powerful tool that can streamline workflow and improve productivity for Linux users.

### Syntax
The basic syntax of the 'at' command is simple:

```
at <time>
```

The time parameter specifies when the command should be run. This can be specified in various formats such as HH:MM, HH:MM YYYY-MM-DD, etc. After entering the 'at' command, you will be prompted to enter the command or script that you want to run at the specified time. Pressing Ctrl+D will save the job and schedule it for execution.

### Examples
1. Running a command at a specific time:
```
$ at 10:00
$ ls -l
Ctrl+D
```
In this example, the 'ls -l' command will be executed at 10:00.

2. Scheduling a script to run at a future date and time:
```
$ at 15:30 2022-12-31
$ /path/to/script.sh
Ctrl+D
```
This will schedule the execution of 'script.sh' at 3:30 PM on December 31, 2022.

3. Running a command at a particular time range:
```
$ at now + 1 hour
$ echo "Task completed"
Ctrl+D
```
This will execute the echo command one hour from the current time.

### Version
The 'at' command has been a part of Linux distributions for many years and is available on most Unix-like systems. It is a built-in command and does not require any additional installations. 

In conclusion, the 'at' command in Linux is a valuable tool for automating tasks and scheduling commands to run at specific times. By understanding its syntax and usage, users can effectively manage their workflow and improve efficiency.