---
title: "[GO] Error Handling and Panic Recovery"
author: 46ebu
date: 2023-11-18 18:58:59 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-error-handling-and-panic-recovery
---

![Intro](/assets/img/post/go.png)
### Introduction
In Go, error handling is a key feature of the language that allows developers to manage unexpected situations and recover gracefully from failures. Error handling in Go is unique compared to other languages because it encourages explicit error checking rather than exceptions. Additionally, panic recovery is another mechanism in Go that allows for handling errors that are unrecoverable.

### Error Handling in Go
In Go, errors are represented by the `error` interface type, which is defined as:
```go
type error interface {
    Error() string
}
```
This interface has a single method `Error() string` that returns a string description of the error. Errors are typically returned as the last return value from a function, and it is common practice to check the error before proceeding further.

### Example 1: Simple Error Handling
```go
package main

import (
    "errors"
    "fmt"
)

func divide(a, b int) (int, error) {
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
In this example, the `divide` function returns an error if the divisor is zero. The `main` function checks for the error and handles it accordingly.

### Panic Recovery in Go
Panic in Go is a built-in function that stops the ordinary flow of control and begins panicking. When a panic occurs, the program starts unwinding the stack, running any deferred functions along the way. To recover from a panic, you can use the `recover` function.

### Example 2: Panic and Recover
```go
package main

import "fmt"

func recoverPanic() {
    if r := recover(); r != nil {
        fmt.Println("Recovered from panic:", r)
    }
}

func main() {
    defer recoverPanic()

    fmt.Println("Start")
    panic("Something went wrong!")
    fmt.Println("End")
}
```
In this example, the `panic` function is called with a message, causing the program to panic. However, the `recoverPanic` function is deferred and invoked to handle the panic.

### Conclusion
Error handling and panic recovery are essential concepts in Go that allow developers to manage errors and failures effectively. By understanding how to handle errors and recover from panics, developers can write more robust and reliable Go programs. It is recommended to always handle errors explicitly and use panic and recover sparingly for critical situations.