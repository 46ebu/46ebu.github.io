---
title: "The Power of firewalld in Linux"
author: 46ebu
date: 2024-03-16 15:29:36 +0900
categories: [linux]
tags: [linux]
render_with_liquid: false
---

![Intro](/assets/img/post/linux.png)
### Introduction to firewalld
Firewalld is a dynamic firewall manager introduced in recent versions of Linux distributions, such as CentOS 7, RHEL 7, and Fedora 21. It is designed as an alternative to the traditional iptables packet filtering system, providing a higher level of abstraction and simplifying the management of firewall rules.

### Basic Concepts
Firewalld uses the concept of zones to categorize network interfaces and determine the level of trust assigned to them. Each zone defines a set of rules that specify which traffic is allowed or denied. The default zone is typically set to public, but users can define custom zones to suit their specific networking needs.

### Managing firewalld
One of the key features of firewalld is its command-line interface, which allows users to interact with the firewall through the terminal. Here are some basic commands that can be used to manage firewalld:

1. Check the status of firewalld:
```bash
sudo systemctl status firewalld
```

2. Start, stop, or restart firewalld:
```bash
sudo systemctl start firewalld
sudo systemctl stop firewalld
sudo systemctl restart firewalld
```

3. Enable firewalld to start on boot:
```bash
sudo systemctl enable firewalld
```

### Configuring firewall rules
Firewalld simplifies the process of creating and managing firewall rules using XML-based configuration files. The rules are defined in the form of services, ports, or source addresses, making it easier to understand and maintain. Here is an example of adding a rule to allow HTTP traffic:

```bash
sudo firewall-cmd --zone=public --add-service=http --permanent
```

In this command, the --zone option specifies the zone where the rule will be applied, while --add-service specifies the service to allow. The --permanent flag ensures that the rule persists across reboots.

### Conclusion
Firewalld provides a user-friendly interface for managing firewall rules in Linux, offering a higher level of abstraction and simplifying the configuration process. By understanding the basic concepts and commands of firewalld, users can effectively secure their network and protect their systems from malicious traffic.