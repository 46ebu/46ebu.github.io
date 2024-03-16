---
title: "[linux] Exploring the 'nm' Command in Linux"
author: 46ebu
date: 2021-09-24 09:45:39 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-exploring-the-nm-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
In the world of Linux, the 'nm' command is a powerful tool that provides detailed information about symbols in object files or libraries. It is used by developers and system administrators to debug and analyze binary files. This command can help identify missing symbols, conflicts, and dependencies within a program.

### Syntax
The syntax of the 'nm' command is straightforward:

```bash
nm [options] <file>
```

Here, 'file' refers to the binary file or library you want to analyze. The 'nm' command comes with various options that allow you to customize the output according to your needs. Some common options include:
- `-A`: Display all symbols, including local
- `-g`: Display only global symbols
- `-C`: demangle C++ symbols
- `-D`: Display dynamic symbols

### Example Codes
1. To display all symbols in a binary file:
```bash
nm -A /path/to/binaryfile
```
This command will show both local and global symbols present in the binary file.

2. To display only global symbols:
```bash
nm -g /path/to/binaryfile
```
Using this command will filter out local symbols and only display global symbols.

3. To demangle C++ symbols in a library:
```bash
nm -C /path/to/library
```
This command will help you easily interpret C++ symbols by demangling them.

### Applicable Versions
The 'nm' command is available on most Unix-like operating systems, including Linux. It is included in the GNU Binutils package, which is a collection of binary tools used for handling object files. The 'nm' command has been around for a long time and is considered a standard tool in the Linux development environment.

### Conclusion
In conclusion, the 'nm' command is a valuable tool for developers and system administrators working with binary files in Linux. By providing detailed information about symbols, it helps in debugging and analyzing programs effectively. Understanding how to use the 'nm' command and its various options can greatly enhance your workflow and productivity in the Linux environment.