---
title: "[linux] An Introduction to Debugging with GDB in Linux"
author: 46ebu
date: 2023-06-04 06:31:38 
categories: [linux]
tags: [linux]
render_with_liquid: false
lang: en
permalink: /linux-an-introduction-to-debugging-with-gdb-in-linux
---

![Intro](/assets/img/post/linux.png)
### What is GDB?

GDB, or GNU Debugger, is a powerful command-line debugger available for various operating systems, including Linux. It allows developers to analyze and debug programs written in languages such as C, C++, and other supported languages. GDB enables users to track down bugs, analyze memory usage, and understand program execution flow by providing tools for inspection and control of running programs.

### Basic Syntax

To start debugging with GDB, you need to compile your code with debugging symbols enabled. For example, if you are compiling a C program with `gcc`, you would include the `-g` flag:

```bash
gcc -g my_program.c -o my_program
```

To start debugging your program, you would run GDB followed by the name of the executable:

```bash
gdb my_program
```

Once inside GDB, you can set breakpoints, examine variables, and step through the program's execution using commands like `break`, `run`, `info variables`, `next`, and `print`.

### Example Codes

Here are three example codes to demonstrate how GDB can be used to debug programs:

1. Setting a breakpoint:
```c
#include <stdio.h>

int main() {
    int x = 10;
    printf("Before breakpoint\n");
    x = x * 2;
    printf("After breakpoint\n");
    return 0;
}
```
Run GDB with the compiled executable and set a breakpoint at line 6 before running the program. When the program execution reaches the breakpoint, you can inspect the variable `x`.

2. Stepping through the program:
```c
#include <stdio.h>

int sum(int a, int b) {
    return a + b;
}

int main() {
    int x = 10;
    int y = 20;
    int result = sum(x, y);
    printf("Result: %d\n", result);
    return 0;
}
```
By using commands like `next` and `step`, you can step through the execution of the program to understand how the `sum` function is called and the result is computed.

3. Examining memory:
```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    int* nums = (int*)malloc(5 * sizeof(int));
    for(int i = 0; i < 5; i++) {
        nums[i] = i * 10;
    }
    free(nums);
    return 0;
}
```
You can use GDB to analyze memory usage, set watchpoints, and debug memory-related issues like memory leaks and segmentation faults.

### Applicable Versions

GDB is constantly evolving, and newer versions may offer additional features and enhancements. The basic usage and commands are consistent across versions, but it's recommended to use the latest stable release for optimal functionality.

By mastering GDB, developers can efficiently debug programs, identify problems, and improve code quality in their Linux projects. Whether you are a beginner or an experienced developer, understanding how to utilize GDB can significantly enhance your debugging skills.