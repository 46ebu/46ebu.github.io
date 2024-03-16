---
title: "[linux] A Deep Dive into firewalld in Linux"
author: 46ebu
date: 2023-03-04 06:45:19 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-a-deep-dive-into-firewalld-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
Firewalld is a dynamic firewall manager for Linux operating systems that dynamically manages the firewall rules. It provides a way to manage firewall rules without having to deal with low-level iptables commands directly. Firewalld operates as a daemon that users can interact with using various command-line tools or graphical interfaces.

### Installing firewalld
Before using firewalld, you need to ensure that it is installed on your system. On most Linux distributions, you can install firewalld using the package manager:
```bash
sudo apt-get install firewalld    # for Ubuntu/Debian
sudo yum install firewalld        # for CentOS/RHEL
```

### Using firewalld
Firewalld uses zones to define the level of trust for a network interface and incoming traffic. Some common zones include public, internal, and trusted. To list the available zones, you can use the `firewall-cmd` command:
```bash
firewall-cmd --get-zones
```

To set a specific zone for a network interface, you can use the following syntax:
```bash
firewall-cmd --zone=public --change-interface=eth0
```
This command would set the network interface `eth0` to be associated with the public zone.

### Managing Rules
Firewalld allows you to manage firewall rules using the `firewall-cmd` command. You can add rules to allow or block specific ports and services or IP addresses. For example, to allow incoming traffic on port 80, you can use the following command:
```bash
firewall-cmd --zone=public --add-port=80/tcp
```

To block incoming traffic from a specific IP address range, you can use:
```bash
firewall-cmd --zone=public --add-rich-rule='rule family="ipv4" source address="192.168.1.0/24" drop'
```

### Reload and Restart
After making changes to the firewall rules, you need to either reload or restart firewalld for the changes to take effect. Reloading the firewall will apply the new rules without disrupting established connections, while restarting the firewall will disconnect all active connections:
```bash
firewall-cmd --reload
firewall-cmd --complete-reload
```

### Conclusion
In conclusion, firewalld is a powerful tool for managing firewall rules in Linux. It provides a more user-friendly interface compared to raw iptables commands and allows for dynamic changes to the firewall configuration. By understanding how to use firewalld effectively, you can better secure your Linux system against unauthorized access and malicious activity.