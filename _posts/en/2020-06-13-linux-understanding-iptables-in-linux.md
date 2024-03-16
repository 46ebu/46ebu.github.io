---
title: "[linux] Understanding iptables in Linux"
author: 46ebu
date: 2020-06-13 23:12:53 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-understanding-iptables-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
Iptables is a user-space utility program that allows a system administrator to configure the IP packet filter rules in the Linux kernel firewall. These rules can help in filtering, forwarding, and altering IP packets. It is a powerful tool for securing a Linux system by controlling network traffic.

### Syntax
The syntax of iptables rules can seem daunting at first, but it follows a simple structure:
- Chain: Specifies which chain to operate on (INPUT, OUTPUT, FORWARD).
- Options: Specify the matching criteria and action to take.
- Criteria: The conditions that must be met for the rule to apply.
- Action: The action to take if the criteria are met (ACCEPT, DROP, REJECT).

### Example Codes
1. Allow SSH traffic:
```
iptables -A INPUT -p tcp --dport 22 -j ACCEPT
```
- This command appends a rule to the INPUT chain that allows TCP traffic on port 22 (SSH) to be accepted.

2. Block a specific IP address:
```
iptables -A INPUT -s 192.168.1.100 -j DROP
```
- This command appends a rule to the INPUT chain that blocks all traffic from the IP address 192.168.1.100.

3. Allow specific IP addresses and deny others:
```
iptables -A INPUT -s 192.168.1.0/24 -j ACCEPT
iptables -A INPUT -s 192.168.2.0/24 -j ACCEPT
iptables -A INPUT -j DROP
```
- The first two commands allow traffic from the IP ranges 192.168.1.0/24 and 192.168.2.0/24, while the third command drops all other traffic.

### Applicable Versions
Iptables has been the standard firewall tool in Linux for many years. However, with the introduction of nftables in later versions of the Linux kernel, iptables is being phased out in favor of nftables. Many modern Linux distributions still use iptables, but it is recommended to learn nftables for future-proofing your firewall configurations.

In conclusion, understanding iptables is essential for any Linux system administrator looking to secure their network. While it may take some time to grasp the syntax and rules, mastering iptables can greatly enhance the security of your system. Remember to always test your rules carefully to avoid unintended consequences.