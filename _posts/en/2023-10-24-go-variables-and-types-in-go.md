---
title: "[GO] Variables and Types in Go"
author: 46ebu
date: 2023-10-24 00:44:02 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-variables-and-types-in-go
---

![Intro](/assets/img/post/go.png)
### Introduction
In the Go programming language, variables and types are fundamental concepts that form the foundation of any program. Understanding how to declare variables and assign types is crucial for writing efficient and readable code. In this blog post, we will explore the syntax and usage of variables and types in Go.

### Declaring Variables
In Go, variables are declared using the `var` keyword followed by the variable name and type. For example, to declare an integer variable named `num`, we can write `var num int`. Variables can also be initialized with a value at the time of declaration like `var num int = 10`. Alternatively, Go can infer the type of the variable based on the assigned value, which allows for shorter declarations like `num := 10`. It's important to note that Go enforces strong typing, meaning that once a variable is declared with a certain type, it cannot be reassigned a value of a different type.

### Example 1: Declaring and Assigning Variables
```go
package main

import "fmt"

func main() {
    var num int
    num = 10
    fmt.Println(num)

    var name string = "John"
    fmt.Println(name)

    city := "New York"
    fmt.Println(city)
}
```

### Data Types
Go supports various data types, including integers, floating-point numbers, strings, booleans, and more. Each data type has a specific range of values and operations that can be performed on it. For example, Go has basic numeric types like `int`, `float64`, and `complex128`, as well as composite types like arrays, slices, maps, and structures. Understanding the different data types available in Go is essential for writing efficient and bug-free code.

### Example 2: Types in Go
```go
package main

import "fmt"

func main() {
    var num int
    num = 10
    fmt.Println(num)

    var price float64 = 99.99
    fmt.Println(price)

    var isActive bool
    isActive = true
    fmt.Println(isActive)
}
```

### Type Conversion
Type conversion in Go allows us to convert a value from one type to another. This can be useful when we want to perform operations between variables of different types. To convert a value to a different type, we can use syntax like `newType(variable)`. It's important to note that Go requires explicit type conversions, and implicit conversions are not allowed to avoid unexpected behavior in the code.

### Example 3: Type Conversion in Go
```go
package main

import "fmt"

func main() {
    num := 10
    price := 99.99

    total := float64(num) + price
    fmt.Println(total)

    isActive := true
    status := "Active"
    fmt.Println(status + " " + fmt.Sprint(isActive))
}
```

### Conclusion
Variables and types are essential components of any Go program, allowing developers to store and manipulate data effectively. By understanding how to declare variables, assign types, and perform type conversions, developers can write robust and efficient code in Go. Embracing strong typing and the rich set of data types in Go can lead to more secure and predictable programs.