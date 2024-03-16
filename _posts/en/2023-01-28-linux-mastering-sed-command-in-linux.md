---
title: "[linux] Mastering 'sed' Command in Linux"
author: 46ebu
date: 2023-01-28 10:01:09 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-mastering-sed-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction to 'sed'

`sed` stands for stream editor and is a powerful utility in Linux used for parsing and transforming text. It processes text line by line and allows for performing various operations like search, replace, insert, delete, etc. on text files or streams. 

One of the key features of `sed` is its ability to use regular expressions for pattern matching, making it a versatile tool for text manipulation tasks.

### Basic Syntax

The basic syntax for using `sed` is as follows:
```bash
sed OPTIONS 'command' filename
```

- OPTIONS: These can be used to modify the behavior of `sed`, like using `-i` to edit files in place.
- 'command': This is the operation you want to perform using `sed`.
- filename: The name of the file to be processed.

### Example Codes

1. Searching and Replacing:
```bash
sed 's/old_text/new_text/g' filename
```
This command replaces all occurrences of 'old_text' with 'new_text' in the file.

2. Deleting Lines:
```bash
sed '/pattern/d' filename
```
This command deletes all lines containing 'pattern' in the file.

3. Inserting Text:
```bash
sed '1i\New_line' filename
```
This command inserts 'New_line' at the beginning of the file.

### Versions and Compatibility

`sed` is a standard Unix utility and is available on all Unix-like systems, including Linux. The GNU version of `sed` is the most common one and offers additional features like extended regular expressions.

As `sed` operates on streams of text, it can be easily integrated into shell scripts and pipelines to automate text processing tasks efficiently.

Mastering `sed` can greatly enhance your text manipulation capabilities in Linux, making it a valuable tool for sysadmins, developers, and anyone working with text files.