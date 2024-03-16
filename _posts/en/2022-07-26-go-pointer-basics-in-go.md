---
title: "[GO] Pointer Basics in Go"
author: 46ebu
date: 2022-07-26 20:49:13 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-pointer-basics-in-go
---

![Intro](/assets/img/post/go.png)
### Introduction
Pointers are a fundamental concept in programming, allowing for more efficient memory management and manipulation of values in Go. Understanding how pointers work in Go is crucial for any developer looking to write efficient and effective code. In this blog post, we will delve into the basics of pointers in Go and explore their syntax, use cases, and best practices.

### Pointer Syntax in Go
In Go, a pointer is represented using the `*` symbol before the type of the variable it points to. For example, to declare a pointer to an integer variable, you would use `var ptr *int`. This declares a pointer variable `ptr` that can point to an integer value. 

### Example Codes
Let's look at a few examples to illustrate how pointers work in Go:

1. **Simple Pointer Example:**
```go
func main() {
    x := 10
    ptr := &x // pointer to x
    fmt.Println("Value of x:", x)
    fmt.Println("Address of x:", &x)
    fmt.Println("Value of ptr:", ptr)
    fmt.Println("Value at address ptr points to:", *ptr)
}
```

In this example, we declare a variable `x` with a value of `10`, and then create a pointer `ptr` that points to the memory address of `x`. We then print out the value of `x`, the address of `x`, the value of `ptr`, and the value at the address `ptr` points to.

2. **Pointer and Function Example:**
```go
func changeValue(ptr *int) {
    *ptr = 20
}

func main() {
    x := 10
    fmt.Println("Before - Value of x:", x)
    changeValue(&x)
    fmt.Println("After - Value of x:", x)
}
```

In this example, we define a function `changeValue` that takes a pointer to an integer as a parameter and updates the value it points to. We then call this function with the address of variable `x`, and observe how the value of `x` changes as a result.

3. **Pointer to Struct Example:**
```go
type Person struct {
    Name string
    Age int
}

func main() {
    p := Person{Name: "Alice", Age: 30}
    ptr := &p
    fmt.Println("Name:", (*ptr).Name)
    fmt.Println("Age:", (*ptr).Age)
}
```

In this example, we define a `Person` struct with `Name` and `Age` fields. We then create a `Person` instance `p`, and a pointer `ptr` that points to `p`. We access the fields of the `Person` struct using the pointer syntax.

### Applicable Versions and Best Practices
Pointers are a powerful tool in Go that can help improve performance and memory management in your programs. It is important to use pointers judiciously and avoid unnecessary pointer arithmetic that can lead to bugs and memory leaks. Understanding the basics of pointers in Go will enable you to write more efficient and reliable code in your Go projects.

In conclusion, pointers are an essential concept in Go programming that allow for more efficient memory management and manipulation of values. By understanding the syntax of pointers, their use cases, and best practices, you can leverage the power of pointers in your Go programs to write more efficient and reliable code.