---
title: "[linux] Delving into the 'bg' Command in Linux"
author: 46ebu
date: 2023-05-25 13:57:49 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-delving-into-the-bg-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction to the 'bg' command
In Linux, the 'bg' command is used to move a suspended job to the background, allowing it to continue running while you work on other tasks in the foreground. When a job is suspended using the 'Ctrl + Z' key combination, it stops running and is placed in the background. The 'bg' command is then used to resume the job in the background.

### Syntax of the 'bg' command
The syntax for the 'bg' command is straightforward. After suspending a job with 'Ctrl + Z', simply type 'bg' followed by the job ID or percent symbol (%) and press Enter. This will move the job to the background and resume its execution.

### Examples of using the 'bg' command
1. Suppose you have a long-running script named 'myscript.sh' that you start but then realize you need to do something else in the terminal. You can suspend the script using 'Ctrl + Z' and then use the 'bg' command to resume it in the background:
```bash
$ ./myscript.sh
^Z
$ bg
```

2. You can also use the job ID to specify which job to move to the background. To view a list of active jobs and their IDs, you can use the 'jobs' command:
```bash
$ jobs
[1]+  Stopped                ./myscript.sh
$ bg %1
```

3. Additionally, you can use the 'bg' command with job IDs to bring multiple jobs into the background simultaneously:
```bash
$ ./job1
^Z
$ ./job2
^Z
$ jobs
[1]+  Stopped                ./job1
[2]+  Stopped                ./job2
$ bg 1 2
```

### Versions and compatibility
The 'bg' command is a built-in command in most Unix-like operating systems, including Linux. It is compatible with all major distributions of Linux, such as Ubuntu, Fedora, CentOS, and Debian. The syntax and functionality of the 'bg' command remain consistent across these distributions.

In conclusion, the 'bg' command in Linux is a useful tool for managing background jobs and effectively utilizing system resources. By understanding how to use the 'bg' command, you can efficiently manage and prioritize tasks within the Linux terminal environment.