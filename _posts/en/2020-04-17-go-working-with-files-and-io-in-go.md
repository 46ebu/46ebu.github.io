---
title: "[GO] Working with Files and I/O in Go"
author: 46ebu
date: 2020-04-17 07:43:39 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-working-with-files-and-io-in-go
---

![Intro](/assets/img/post/go.png)
### Introduction
Working with files and Input/Output (I/O) operations is essential in any programming language for tasks such as reading and writing data. In Go, a programming language developed by Google, handling files and I/O is straightforward with the built-in `os` and `io` packages.

### Reading a File
To read a file in Go, you can use the `os.Open` function to open the file and `os.Read` function to read its contents. Here is an example code snippet:

```go
package main

import (
    "os"
    "fmt"
)

func main() {
    file, err := os.Open("example.txt")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    defer file.Close()
    
    data := make([]byte, 100)
    n, err := file.Read(data)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    fmt.Println(string(data[:n]))
}
```

### Writing to a File
To write to a file in Go, you can use the `os.Create` function to create a new file and `os.Write` function to write data to it. Here is an example code snippet:

```go
package main

import (
    "os"
    "fmt"
)

func main() {
    file, err := os.Create("output.txt")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    defer file.Close()
    
    text := []byte("Hello, World!")
    _, err = file.Write(text)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    fmt.Println("Data written to file successfully!")
}
```

### Reading and Writing with bufio Package
The `bufio` package in Go provides buffered I/O for efficient reading and writing. Here is an example code snippet demonstrating how to use `bufio` for reading and writing:

```go
package main

import (
    "os"
    "bufio"
    "fmt"
)

func main() {
    file, err := os.Open("example.txt")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    defer file.Close()
    
    scanner := bufio.NewScanner(file)
    for scanner.Scan() {
        fmt.Println(scanner.Text())
    }
    
    newFile, err := os.Create("output.txt")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    defer newFile.Close()
    
    writer := bufio.NewWriter(newFile)
    _, err = writer.WriteString("Hello, World!")
    if err != nil {
        fmt.Println("Error:", err)
        return
    }
    
    writer.Flush()
    fmt.Println("Data written to file successfully!")
}
```

Overall, working with files and I/O in Go is straightforward thanks to the built-in packages provided for these operations. By using functions from the `os`, `io`, and `bufio` packages, you can easily read from and write to files in Go. The examples provided illustrate the basic file handling operations in Go, showcasing how to read and write data efficiently in a Go program.