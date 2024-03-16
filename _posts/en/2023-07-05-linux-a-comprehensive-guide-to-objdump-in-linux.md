---
title: "[linux] A Comprehensive Guide to objdump in Linux"
author: 46ebu
date: 2023-07-05 11:31:47 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-a-comprehensive-guide-to-objdump-in-linux
---

![Intro](/assets/img/post/linux.png)
### Introduction to objdump

Objdump is a command-line utility in Linux that is part of the GNU Binutils suite. It is used for displaying information about object files such as executable, shared objects, and static libraries. Objdump can provide information about various aspects of the object file including file headers, sections, symbols, and disassembled machine code instructions.

### Syntax and Usage

The syntax for objdump is as follows:
```
objdump [options] [filename]
```
Some common options used with objdump include:
- -f: Display file header information
- -s: Display full contents of sections
- -t: Display symbol table
- -d: Disassemble the file's contents
- -x: Display all available header information

### Example Codes

1. To display the file header information of an executable:
```
objdump -f executable
```

2. To display the disassembled machine code of an executable:
```
objdump -d executable
```

3. To display the symbol table of an executable:
```
objdump -t executable
```

### Versions and Compatibility

Objdump is a standard utility in most Linux distributions and is available on platforms such as x86, ARM, and MIPS. It supports various object file formats including ELF, COFF, PE, and Mach-O. Objdump can be used to analyze both 32-bit and 64-bit object files.

In conclusion, objdump is a powerful tool for analyzing and inspecting object files in Linux. It provides detailed information about the structure and contents of executable files, shared objects, and static libraries. By using objdump with the appropriate options, developers can gain insights into the inner workings of their programs and debug any issues that may arise.