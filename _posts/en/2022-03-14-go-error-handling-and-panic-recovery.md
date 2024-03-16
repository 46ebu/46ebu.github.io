---
title: "[GO] Error Handling and Panic Recovery"
author: 46ebu
date: 2022-03-14 17:26:45 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-error-handling-and-panic-recovery
---

![Intro](/assets/img/post/go.png)
### Introduction
In Go programming language, error handling is a crucial aspect of writing robust and reliable code. Errors are represented as values in Go and are handled using the `error` interface. Additionally, Go provides a mechanism called panic and recover for managing catastrophic errors that can halt the program execution.

### Error Handling
In Go, errors are values that are returned by functions to indicate that something has gone wrong. The `error` interface is a built-in type in Go that defines a method `Error()` which returns a string describing the error. Errors are commonly handled using `if` statements to check for the presence of an error and handle it appropriately.

### Example 1: Simple Error Handling
```go
package main

import (
    "fmt"
    "errors"
)

func divide(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("division by zero")
    }

    return a / b, nil
}

func main() {
    result, err := divide(10, 0)
    if err != nil {
        fmt.Println("Error:", err)
        return
    }

    fmt.Println("Result:", result)
}
```
In this example, the `divide` function returns an error if the divisor `b` is zero. The `main` function checks for the error and prints an error message if one occurs.

### Panic and Recover
Sometimes, an unrecoverable error occurs that causes the program to panic and stop execution. In Go, panicking is a built-in function that can be triggered using the `panic` keyword. However, Go provides a way to recover from a panic using the `recover` function.

### Example 2: Panic and Recover
```go
package main

import "fmt"

func recoverPanic() {
    if r := recover(); r != nil {
        fmt.Println("Recovered from panic:", r)
    }
}

func divide(a, b float64) float64 {
    defer recoverPanic()
    
    if b == 0 {
        panic("division by zero")
    }

    return a / b
}

func main() {
    result := divide(10, 0)
    fmt.Println("Result:", result)
}
```
In this example, the `divide` function panics if the divisor `b` is zero. However, the panic is caught and recovered by the `recoverPanic` function, allowing the program to continue execution.

### Conclusion
Error handling and panic recovery are essential techniques in Go for building robust and reliable applications. By properly handling errors and managing panics, developers can ensure that their code is resilient to unexpected failures and can gracefully recover from catastrophic errors.