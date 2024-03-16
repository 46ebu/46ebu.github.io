---
title: "[linux] Understanding the 'fg' Command"
author: 46ebu
date: 2023-09-28 15:40:18 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-understanding-the-fg-command
---

![Intro](/assets/img/post/linux.png)
### Introduction
In Linux, the `fg` command is used to bring a background job to the foreground. When a process is running in the background and you want to interact with it, you can use `fg` to switch it to the foreground. This can be useful when you have multiple tasks running simultaneously and need to prioritize one over the others.

### Syntax
The basic syntax of the `fg` command is:
```
fg [job_spec]
```
Here, `job_spec` is the job ID of the background process you want to bring to the foreground. If you do not specify a `job_spec`, the last background process started will be brought to the foreground.

### Examples
1. Bringing the last background process to the foreground:
```
$ sleep 60 &
[1] 1234
$ fg
```
In this example, the `sleep 60` process is started in the background and its job ID is 1. The `fg` command brings this process to the foreground.

2. Bringing a specific background process to the foreground:
```
$ sleep 120 &
[2] 5678
$ fg 2
```
Here, the `sleep 120` process is started in the background with job ID 2. By specifying `2` after the `fg` command, we bring this specific process to the foreground.

3. Using `fg` with job control:
```
$ vi filename.txt
Ctrl + Z
$ bg
$ fg
```
In this example, we start editing a file with `vi` and suspend the process with `Ctrl + Z`. Then, we resume it in the background with `bg` and finally bring it back to the foreground with `fg`.

### Applicable Versions
The `fg` command is a part of the GNU Core Utilities package which is available on most Linux distributions. It can be used on systems running bash or other compatible shells.

Overall, the `fg` command is a handy tool for managing background processes in a Linux environment. Whether you need to prioritize a certain task or interact with a background process, `fg` allows you to easily bring it to the foreground and continue working on it seamlessly.