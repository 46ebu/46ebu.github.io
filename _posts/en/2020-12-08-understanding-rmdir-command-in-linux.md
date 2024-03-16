---
title: "Understanding 'rmdir' Command in Linux"
author: 46ebu
date: 2020-12-08 23:49:07 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /understanding-rmdir-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction to 'rmdir'

The 'rmdir' command in Linux is used to remove empty directories. It stands for "remove directory". Unlike the 'rm' command which is used to remove files, 'rmdir' specifically deals with directories. It is a safe way to delete directories as it won't work if the directory is not empty. 

### Syntax

The syntax of the 'rmdir' command is simple:
```
rmdir [option] directory_name
```

### Examples 

1. To remove an empty directory named "example":
```
rmdir example
```

2. To remove multiple empty directories:
```
rmdir dir1 dir2 dir3
```

3. To force remove a non-empty directory:
```
rmdir -rf directory_name
```

### Options

Some commonly used options with the 'rmdir' command include:
- '-p': Removes parent directories as well if they become empty after removing the specified directory.
- '-v': Displays a message for each directory that is removed.
- '--ignore-fail-on-non-empty': Ignores the error if the directory is not empty and continues with the removal.

### Versions

The 'rmdir' command is available on most Linux distributions and Unix systems. It is a standard command line utility and can be used in various scripts and commands for directory management.

### Conclusion

In conclusion, the 'rmdir' command in Linux provides a simple and safe way to remove empty directories. It is a useful tool for managing directory structures and organizing files on a system. By understanding its syntax and options, users can efficiently remove directories as needed.