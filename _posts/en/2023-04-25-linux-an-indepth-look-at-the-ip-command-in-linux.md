---
title: "[linux] An In-depth Look at the 'ip' Command in Linux"
author: 46ebu
date: 2023-04-25 06:12:29 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-an-indepth-look-at-the-ip-command-in-linux
---

![Intro](/assets/img/post/linux.png)
IP command in Linux is a versatile tool used primarily for network administration. It provides a way to view and configure network interfaces, routing, and tunnels on a system. The IP command is part of the iproute2 package and is more powerful and flexible compared to the older ifconfig command. In this blog post, we will explore the different functionalities of the IP command and how it can be used for various networking tasks.

### Viewing Network Interfaces
The IP command can be used to display information about network interfaces on a system. To view a list of all interfaces, you can use the following command:
```
ip link show
```
This will show all network interfaces along with their state, MAC address, and other relevant information.

### Configuring Network Interfaces
The IP command can also be used to configure network interfaces. For example, to assign an IP address to an interface, you can use the following command:
```
ip address add 192.168.1.10/24 dev eth0
```
This command will assign the IP address 192.168.1.10 with a subnet mask of /24 to the interface eth0.

### Managing Routing Tables
Another important use of the IP command is to manage routing tables on a system. You can add, delete, or modify routes using the IP command. For example, to add a default route, you can use the following command:
```
ip route add default via 192.168.1.1
```
This command will add a default route via the gateway 192.168.1.1 to the routing table.

### Applicable Versions
The IP command is available in most modern Linux distributions and is a part of the iproute2 package. It is recommended to use the IP command for network configuration and administration tasks as it provides more functionality and features compared to the older networking tools.

In conclusion, the IP command in Linux is a powerful tool for network administration and configuration. It can be used to view and configure network interfaces, manage routing tables, and perform various networking tasks. With its flexibility and versatility, the IP command is a valuable resource for system administrators and network engineers looking to efficiently manage their network infrastructure.