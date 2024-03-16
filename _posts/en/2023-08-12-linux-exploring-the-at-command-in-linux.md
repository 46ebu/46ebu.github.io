---
title: "[Linux] Exploring the 'at' Command in Linux"
author: 46ebu
date: 2023-08-12 09:31:58 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-exploring-the-at-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Overview

In Linux, the 'at' command is used to schedule tasks to be executed at a specific time. This command allows users to run a command or a script once at a specified time in the future. The 'at' command is particularly useful for performing tasks that should be executed at a later time without the need to be continuously active. 

### Syntax

The basic syntax for the 'at' command is as follows:

```shell
at TIME
```

Where TIME is the time at which the task should be executed. This time can be specified in various formats such as HH:MM, midnight, tomorrow, etc.

### Examples

1. Scheduling a Task:
```shell
echo "echo Hello, World!" | at 10:30pm
```
This command will run the "echo Hello, World!" script at 10:30 PM.

2. Using a Script:
```shell
at 2:00pm -f script.sh
```
This command will execute the script.sh file at 2:00 PM.

3. Listing Scheduled Tasks:
```shell
atq
```
This command is used to list the tasks that have been scheduled using the 'at' command.

### Versions

The 'at' command is available on most Linux distributions. However, it may not be installed by default on some systems. Users can install the 'at' command using their package manager. 

### Conclusion

The 'at' command in Linux is a powerful tool for scheduling tasks to be executed at a specific time in the future. By using the 'at' command, users can automate tasks that need to be run once at a later time without the need for continuous manual intervention. With its simple syntax and versatility, the 'at' command is a valuable asset for Linux users looking to streamline their workflow and improve their productivity.