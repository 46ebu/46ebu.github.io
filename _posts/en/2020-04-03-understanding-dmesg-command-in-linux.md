---
title: "Understanding 'dmesg' Command in Linux"
author: 46ebu
date: 2020-04-03 04:00:11 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /understanding-dmesg-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
The 'dmesg' command in Linux is a powerful tool that displays the message buffer of the kernel. This provides valuable information about the system's hardware, drivers, and kernel modules. By analyzing the output of 'dmesg', users can troubleshoot hardware issues, identify driver problems, and monitor system activity.

### Syntax
The basic syntax of the 'dmesg' command is simple:
```
dmesg
```
This command will display the kernel's message buffer from the current boot session. The output will include messages related to hardware detection, driver loading, and other kernel events. Users can also filter the output by using various options such as '-c' to clear the buffer or '-w' to continuously monitor new messages.

### Examples
1. Displaying the last 20 lines of the kernel message buffer:
```
dmesg | tail -n 20
```
This command will show the last 20 lines of the 'dmesg' output, which can be useful for quickly checking the most recent kernel events without scrolling through the entire buffer.

2. Filtering messages related to a specific hardware component:
```
dmesg | grep 'eth0'
```
This command will only display messages containing the string 'eth0', which is commonly used to refer to Ethernet network interfaces. By filtering the output in this way, users can focus on specific hardware components or events.

3. Monitoring for new messages in real-time:
```
dmesg -w
```
With the '-w' option, the 'dmesg' command will continuously monitor the kernel message buffer and display new messages as they occur. This can be helpful for troubleshooting issues that are occurring in real-time.

### Applicable Versions
The 'dmesg' command is available in all modern Linux distributions and is a standard tool for system administrators, developers, and users. It is part of the 'util-linux' package and is typically pre-installed on most Linux systems.

### Conclusion
In conclusion, the 'dmesg' command is a versatile tool for monitoring and troubleshooting the kernel message buffer in Linux. By understanding how to use 'dmesg' effectively, users can gain valuable insights into system hardware, drivers, and kernel events. Whether diagnosing hardware issues or monitoring system activity, 'dmesg' is an essential command for any Linux user.