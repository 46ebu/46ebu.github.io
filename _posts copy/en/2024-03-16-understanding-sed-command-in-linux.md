---
title: "Understanding 'sed' Command in Linux"
author: 46ebu
date: 2024-03-16 15:25:53 +0900
categories: [linux]
tags: [linux]
render_with_liquid: false
---

![Intro](/assets/img/post/linux.png)
### Introduction to 'sed'

The 'sed' command in Linux stands for "stream editor" and is a powerful text processing tool that is used to perform basic text transformations on an input stream. It is a non-interactive text editor that reads text from a file or standard input, performs editing operations, and then displays the results to standard output. 'sed' allows users to manipulate text using regular expressions and various commands.

### Syntax of 'sed'

The basic syntax of the 'sed' command is as follows: 

```
sed [options] 'command' filename
```

Here are some common options used with 'sed':

- `-n`: Suppresses automatic printing of the pattern space.
- `-e`: Allows to specify multiple commands or scripts.
- `-i`: Edits files in place.

### Example Codes

#### 1. Print lines containing a specific pattern:
The following command will print all lines in a file that contain the word "Linux":

```
sed -n '/Linux/p' file.txt
```
- In this command, `/Linux/` is the regular expression pattern to be matched, and `p` is the command to print the matched lines.

#### 2. Replace specific text in a file:
To replace all occurrences of "oldtext" with "newtext" in a file, you can use the following command:

```
sed -i 's/oldtext/newtext/g' file.txt
```
- Here, `s/oldtext/newtext/g` is the substitution command to replace "oldtext" with "newtext" globally in the file.

#### 3. Delete lines containing a specific pattern:
To delete all lines in a file that contain the word "delete", you can use the following command:

```
sed '/delete/d' file.txt
```
- In this command, `/delete/` specifies the pattern to match, and `d` is the command to delete those lines.

### Versions and Compatibility

The 'sed' command is a standard Unix utility and is available on most Unix-like operating systems, including Linux. It follows POSIX standards, making it compatible with various versions of Unix and Linux distributions. Users can rely on 'sed' for text processing tasks across different platforms without worrying about compatibility issues.

In conclusion, 'sed' is a versatile command-line tool for text processing in Linux, offering a range of functions for manipulating text using regular expressions and commands. By mastering the 'sed' command, users can efficiently edit, transform, and manipulate text files in a streamlined and efficient manner.