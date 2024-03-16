---
title: "[linux] An In-depth Look at the 'head' Command in Linux"
author: 46ebu
date: 2022-11-10 11:16:03 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-an-indepth-look-at-the-head-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction
The 'head' command in Linux is a useful utility that allows users to display the first few lines of a file. It is commonly used to preview the contents of a file without having to open the entire file. In this blog post, we will explore the various ways in which the 'head' command can be used in Linux.

### Syntax
The basic syntax of the 'head' command is as follows:
```
head [OPTIONS] [FILE]
```
Where OPTIONS can be used to specify the number of lines to be displayed and other settings, and FILE is the name of the file whose contents need to be displayed.

### Examples
1. Display the first 10 lines of a file:
```
head file.txt
```
This command will display the first 10 lines of the file.txt.

2. Display a specific number of lines from a file:
```
head -n 5 file.txt
```
This command will display the first 5 lines of the file.txt.

3. Display the first 10 lines of multiple files:
```
head file1.txt file2.txt file3.txt
```
This command will display the first 10 lines of all the specified files.

### Options
The 'head' command comes with several options that allow users to customize its behavior:
- -c, --bytes: Display the first N bytes of each file
- -n, --lines: Display the first N lines of each file
- -q, --quiet: Suppresses the display of file headers
- -v, --verbose: Always display file headers

### Versions
The 'head' command is available in most Unix-like operating systems, including Linux. It is a part of the GNU Core Utilities package and is also available on macOS. Users can refer to the man page for detailed information on the available options and usage examples.

### Conclusion
In conclusion, the 'head' command in Linux is a versatile tool for quickly previewing the contents of files. By using the various options available with the command, users can tailor the output to their specific requirements. Whether you need to check the first few lines of a log file or preview the contents of a text document, the 'head' command is a handy utility to have in your arsenal.