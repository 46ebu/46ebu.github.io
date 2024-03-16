---
title: "[GO] Working with Files and I/O in Go"
author: 46ebu
date: 2020-08-14 05:42:03 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-working-with-files-and-io-in-go
---

![Intro](/assets/img/post/go.png)
### Introduction
Working with files and performing Input/Output operations is a crucial aspect of any programming language. In Go, there are built-in functionalities and packages that make working with files and I/O operations easy and efficient. This blog post will explore how to work with files and perform I/O operations in Go.

### Opening and Reading Files
In Go, the `os` package provides functions for working with files. To open a file, you can use the `os.Open()` function which returns a file descriptor and an error. You can then read the contents of the file using the `bufio` package, which provides buffered I/O operations.

```go
package main

import (
	"bufio"
	"fmt"
	"os"
)

func main() {
	file, err := os.Open("example.txt")
	if err != nil {
		fmt.Println("Error opening file:", err)
		return
	}
	defer file.Close()

	scanner := bufio.NewScanner(file)
	for scanner.Scan() {
		fmt.Println(scanner.Text())
	}
}
```

### Writing to Files
To write to a file in Go, you can use the `os.Create()` function to create a new file or truncate an existing file. You can then write to the file using the `bufio.Writer`. Don't forget to close the file after writing to ensure the data is flushed.

```go
package main

import (
	"bufio"
	"fmt"
	"os"
)

func main() {
	file, err := os.Create("output.txt")
	if err != nil {
		fmt.Println("Error creating file:", err)
		return
	}
	defer file.Close()

	writer := bufio.NewWriter(file)
	fmt.Fprintln(writer, "Hello, World!")
	writer.Flush()
}
```

### Reading and Writing JSON
Go provides a convenient way to work with JSON data using the `encoding/json` package. You can easily read JSON data from a file and decode it into a struct, or encode a struct into JSON data and write it to a file.

```go
package main

import (
	"encoding/json"
	"fmt"
	"os"
)

type Person struct {
	Name string `json:"name"`
	Age  int    `json:"age"`
}

func main() {
	// Reading JSON data from a file
	file, err := os.Open("person.json")
	if err != nil {
		fmt.Println("Error opening file:", err)
		return
	}
	defer file.Close()

	var person Person
	json.NewDecoder(file).Decode(&person)
	fmt.Println("Name:", person.Name)
	fmt.Println("Age:", person.Age)

	// Writing JSON data to a file
	newPerson := Person{Name: "Alice", Age: 30}
	newFile, _ := os.Create("new_person.json")
	defer newFile.Close()

	json.NewEncoder(newFile).Encode(newPerson)
}
```

In this blog post, we have covered the basics of working with files and performing I/O operations in Go. By using the `os` package for file operations and `bufio` package for buffered I/O, you can efficiently read from and write to files. Additionally, the `encoding/json` package makes it easy to work with JSON data. Get started with file handling and I/O operations in Go to enhance your programming skills.