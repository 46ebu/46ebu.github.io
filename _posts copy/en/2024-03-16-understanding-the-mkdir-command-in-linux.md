---
title: "Understanding the 'mkdir' command in Linux"
author: 46ebu
date: 2024-03-16 15:26:12 +0900
categories: [linux]
tags: [linux]
render_with_liquid: false
---

![Intro](/assets/img/post/linux.png)
### Introduction
The 'mkdir' command in Linux is used to create directories or folders in the file system. It stands for 'make directory' and is a basic utility that comes pre-installed on almost all Linux distributions. The command allows users to create directories with specified names in the specified path.

### Syntax
The syntax of the 'mkdir' command is straightforward:
```bash
mkdir [OPTION]... DIRECTORY...
```
Here, the 'OPTION' flag can be used to modify the behavior of the command, while 'DIRECTORY' specifies the name of the directory to be created.

### Examples
1. Creating a single directory:
To create a directory named 'documents' in the current directory, simply run:
```bash
mkdir documents
```
2. Creating multiple directories:
You can also create multiple directories at once by providing multiple directory names as arguments:
```bash
mkdir directory1 directory2 directory3
```
3. Creating directories with parent directories:
If you want to create a directory along with its parent directories, you can use the '-p' flag. For example:
```bash
mkdir -p parent/child/grandchild
```
This will create a directory structure like parent/child/grandchild, even if the parent directory does not exist.

### Options
The 'mkdir' command offers several options to customize its behavior:
- '-p': Create parent directories if they do not exist.
- '-m': Set the permissions of the newly created directories.
- '--mode': Specify the permissions explicitly in octal format.
- '-v': Display a message for each directory created.

### Versions
The 'mkdir' command is a standard utility in the GNU Core Utilities package, which is present in most Linux distributions by default. It is available in all versions of Linux and can be used in both terminal and shell scripts.

### Conclusion
In conclusion, the 'mkdir' command is a useful tool for creating directories in a Linux file system. It is simple to use, versatile, and offers various options to tailor the directory creation process to your needs. Whether you need to create a single directory or a complex directory structure, the 'mkdir' command has got you covered.