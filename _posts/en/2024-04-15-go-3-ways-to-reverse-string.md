---
title: "[go] 3 ways to reverse string"
author: 46ebu
date: 2024-04-15 07:36:44 +0000
categories: [go]
tags: [go]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### Introduction
In Go, reversing a string can be done in multiple ways using different techniques. In this blog post, we will explore three different methods to reverse a string in Go.

### Method 1: Using the Built-in functions
One of the simplest ways to reverse a string in Go is by utilizing the built-in functions provided by the language. The `strings` package in Go provides a function called `Reverse` which can be used to reverse a string. 

```go
package main

import (
	"fmt"
	"strings"
)

func main() {
	str := "hello"
	reversed := strings.Join(strings.Split(str, ""), "")
	fmt.Println(reversed)
}
```

In this code snippet, we first split the string into individual characters using `strings.Split`, then reverse the order using `strings.Join`. The output of this code will be "olleh".

### Method 2: Using a loop
Another way to reverse a string in Go is by using a loop to iterate through the characters of the string and construct a new string in reverse order.

```go
package main

import "fmt"

func reverseString(str string) string {
	runes := []rune(str)
	reversed := make([]rune, len(runes))

	for i, j := 0, len(runes)-1; i < len(runes); i, j = i+1, j-1 {
		reversed[i] = runes[j]
	}

	return string(reversed)
}

func main() {
	str := "hello"
	reversed := reverseString(str)
	fmt.Println(reversed)
}
```

In this code snippet, we convert the string into a slice of runes to handle Unicode characters properly. We then iterate through the characters of the string and construct a new string in reverse order. The output of this code will be "olleh".

### Method 3: Using Recursion
The third method to reverse a string in Go is by using recursion. Recursion is a programming technique where a function calls itself to solve smaller instances of the problem.

```go
package main

import "fmt"

func reverseString(str string) string {
	if len(str) == 0 {
		return str
	}
	return reverseString(str[1:]) + string(str[0])
}

func main() {
	str := "hello"
	reversed := reverseString(str)
	fmt.Println(reversed)
}
```

In this code snippet, we define a function `reverseString` which takes a string as input. The function checks if the length of the string is zero, and if so, returns an empty string. Otherwise, it calls itself recursively to reverse the substring starting from the second character and appends the first character at the end. The output of this code will be "olleh".

### Conclusion
In this blog post, we explored three different methods to reverse a string in Go. Each method offers a unique approach to solving the problem, from using built-in functions to loops and recursion. Depending on the requirements of the application, you can choose the most suitable method to reverse a string efficiently in Go.