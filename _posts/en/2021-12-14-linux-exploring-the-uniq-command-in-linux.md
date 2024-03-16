---
title: "[linux] Exploring the 'uniq' command in Linux"
author: 46ebu
date: 2021-12-14 08:07:23 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-exploring-the-uniq-command-in-linux
---

![Intro](/assets/img/post/linux.png)
### What is 'uniq' command?
The 'uniq' command in Linux is used to filter out adjacent repeated lines in a file. It helps in identifying, removing or counting duplicate lines in a sorted file. The command reads an input file or standard input and writes to standard output while filtering out adjacent matching lines.

### Syntax
The basic syntax for the 'uniq' command is: 
```
uniq [OPTION]... [INPUT [OUTPUT]]
```
Here, the options can include -c for counting occurrences, -d for showing only duplicate lines, -u for showing only unique lines, etc.

### Examples
1. To remove duplicate lines in a file:
```
cat file.txt | sort | uniq > output.txt
```
This code reads the file "file.txt", sorts it, removes any adjacent duplicate lines, and writes the output to "output.txt".

2. Count the number of occurrences for each unique line in a file:
```
sort file.txt | uniq -c
```
This code sorts the file "file.txt" and then counts the number of occurrences for each unique line.

3. Show only the duplicated lines in a file:
```
sort file.txt | uniq -d
```
This code sorts the file "file.txt" and shows only the duplicate lines present in the file.

### Versions
The 'uniq' command is a part of the GNU Core Utilities package and is available on most Linux distributions. It may have slight variations in functionality or options depending on the specific version of the command installed on the system.

In conclusion, the 'uniq' command in Linux is a handy tool for identifying and managing duplicate lines in input files. With its various options, it provides flexibility in filtering and counting duplicate or unique lines based on requirements.