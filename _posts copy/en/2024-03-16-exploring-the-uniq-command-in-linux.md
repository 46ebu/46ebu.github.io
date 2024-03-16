---
title: "Exploring the uniq Command in Linux"
author: 46ebu
date: 2024-03-16 15:34:37 +0900
categories: [linux]
tags: [linux]
render_with_liquid: false
---

![Intro](/assets/img/post/linux.png)
### Overview
The `uniq` command in Linux is used to report or filter out repeated lines in a file. It helps in identifying unique lines or removing duplicate lines within a file. It is a handy tool for data processing and analysis in scripting or command-line tasks.

### Syntax
The basic syntax of the `uniq` command is:
```
uniq [options] [input_file [output_file]]
```

### Examples
1. The following command reads a file named `data.txt`, removes duplicate adjacent lines, and writes the result to `output.txt`:
```
uniq data.txt output.txt
```
2. To count the number of occurrences of duplicate lines in a file, you can use the `-c` option:
```
uniq -c data.txt
```
3. Combining `sort` and `uniq` commands can help in finding unique lines in a sorted file:
```
sort data.txt | uniq
```

### Options
- `-c`: Precede each output line with the count of the number of times the line occurred in the input.
- `-d`: Only output lines that are repeated in the input.
- `-i`: Ignore differences in case when comparing lines.
- `-u`: Only output lines that are unique in the input.
- `-f N`: Skip the first N fields on each line before checking for uniqueness.
- `-s N`: Skip the first N characters on each line before checking for uniqueness.

### Versions
The `uniq` command is standard in most Unix-like operating systems, including Linux distributions. It is part of the GNU Core Utilities package, ensuring its availability on most systems. It has been around for a long time and is a stable and reliable tool for handling duplicate lines in files.

In conclusion, the `uniq` command in Linux provides a simple yet powerful way to identify and process unique or duplicate lines in a file. By understanding its syntax, options, and examples, users can efficiently manage data processing tasks on the command line.