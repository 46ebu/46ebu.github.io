---
title: "[linux] A Guide to Ifconfig in Linux"
author: 46ebu
date: 2023-02-27 22:50:02 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-a-guide-to-ifconfig-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
Ifconfig stands for "interface configuration" and is a command-line utility in Unix-like operating systems, including Linux, that allows users to configure network interfaces on a Linux system. It displays information related to your network interfaces like IP addresses, MAC addresses, network masks, and more. In this blog post, we will delve into the workings of ifconfig and how to use it effectively on a Linux system.

### Syntax
The basic syntax for using ifconfig is as follows:
```bash
ifconfig [interface] [options]
```
Here, "interface" refers to the network interface you want to configure or display information for, such as eth0 or wlan0. The "options" can be used to perform specific tasks like assigning an IP address or netmask to an interface, bringing an interface up or down, and more.

### Example Codes
1. To display information about all network interfaces:
```bash
ifconfig
```
This command will show details for all active network interfaces on your system, including IP addresses, MAC addresses, and network masks.

2. To bring a network interface up or down:
```bash
sudo ifconfig eth0 up
sudo ifconfig eth0 down
```
In these commands, you can replace "eth0" with the interface you want to bring up or down. Bringing an interface up enables networking on that interface, while bringing it down disables networking.

3. To assign an IP address to a network interface:
```bash
sudo ifconfig eth0 192.168.1.10 netmask 255.255.255.0
```
In this example, we assign the IP address 192.168.1.10 with a netmask of 255.255.255.0 to the eth0 interface. This command configures the interface to use the specified IP address and netmask.

### Versions and Alternatives
Ifconfig has been deprecated in many Linux distributions in favor of newer tools like ip and netplan. Despite this, ifconfig is still widely used and available on most systems for compatibility. Users who are comfortable with ifconfig may continue to use it, but it is recommended to familiarize yourself with newer networking tools for long-term compatibility and support.

In conclusion, ifconfig is a powerful tool for configuring and managing network interfaces on a Linux system. It provides essential networking information and allows users to control various network settings. By understanding the syntax and examples provided in this guide, you can effectively use ifconfig to manage your network interfaces in Linux.