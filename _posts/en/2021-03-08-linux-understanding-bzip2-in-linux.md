---
title: "[linux] Understanding bzip2 in Linux"
author: 46ebu
date: 2021-03-08 10:24:21 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-understanding-bzip2-in-linux
---

![Intro](/assets/img/post/linux.png)
### What is bzip2?
bzip2 is a freely available program for compressing and decompressing files in Unix-like operating systems like Linux. It uses the Burrows-Wheeler block-sorting text compression algorithm and Huffman coding for final compression. This results in significantly smaller file sizes compared to the original files.

### Syntax and Usage
The syntax for using bzip2 is simple and straightforward. To compress a file, you can use the following command:
```
bzip2 filename
```
This command will compress the specified file and create a new file with the ".bz2" extension.

To decompress a file that has been compressed using bzip2, you can use the following command:
```
bunzip2 filename.bz2
```
This command will decompress the specified file and restore it to its original state.

### Example Codes
1. Compressing a file:
```
bzip2 example.txt
```

2. Decompressing a file:
```
bunzip2 example.txt.bz2
```

3. Using bzip2 with tar to compress directories:
```
tar cvf - directory/ | bzip2 > directory.tar.bz2
```

### Applicable Versions
bzip2 is a widely supported program and is included in most Linux distributions by default. You can check if it is installed on your system by running the following command:
```
bzip2 --version
```
This will display the version of bzip2 installed on your system.

In conclusion, bzip2 is a powerful tool for compressing and decompressing files in Linux. By understanding its syntax and usage, you can effectively manage file sizes and improve storage efficiency on your system.