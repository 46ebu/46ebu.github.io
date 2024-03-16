---
title: "[linux] An In-depth Look at the 'nm' Command in Linux"
author: 46ebu
date: 2023-02-16 17:36:02 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-an-indepth-look-at-the-nm-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
The 'nm' command in Linux is a powerful tool used to display symbol information in object files. This command is often used by developers and system administrators to analyze binaries and libraries. In this blog post, we will delve into the details of the 'nm' command, its syntax, options, and examples of how it can be used effectively.

### Syntax
The syntax of the 'nm' command is as follows:
```bash
nm [options] [file...]
```
Here, 'options' are the different flags you can use with the 'nm' command, and 'file' refers to the object files you want to analyze. The 'nm' command can be used with various options to extract specific information about symbols in an object file.

### Examples
1. Display all symbols in an object file:
```bash
nm object_file.o
```
This command will display a list of all symbols found in the object file 'object_file.o', including their addresses and types.

2. Display only external symbols in an object file:
```bash
nm -g object_file.o
```
The '-g' option tells 'nm' to only display global (external) symbols from the object file 'object_file.o'.

3. Display the size of symbols in an object file:
```bash
nm -S object_file.o
```
Using the '-S' option with 'nm' will display the size of each symbol in the object file 'object_file.o'.

### Versions
The 'nm' command is a part of the GNU Binutils package and is available on most Linux distributions. It works with various file formats, including ELF (Executable and Linkable Format) and COFF (Common Object File Format). The capabilities of 'nm' may vary slightly depending on the version of the Binutils package installed on your system.

### Conclusion
In conclusion, the 'nm' command in Linux is a versatile tool for analyzing object files and libraries. By understanding its syntax and options, you can extract valuable information about symbols and their properties. Whether you are a developer debugging your code or a system administrator troubleshooting library dependencies, the 'nm' command can be a valuable asset in your toolkit.