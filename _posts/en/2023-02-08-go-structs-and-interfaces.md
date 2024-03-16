---
title: "[GO] Structs and Interfaces"
author: 46ebu
date: 2023-02-08 23:05:35 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-structs-and-interfaces
---

![Intro](/assets/img/post/go.png)
### Overview
In Go, structs are composite data types used to group together different types of data under a single name. They are similar to classes in object-oriented programming languages. Interfaces, on the other hand, define a set of methods that a type must implement. They allow for polymorphism in Go, enabling different types to be used interchangeably.

### Structs
A struct is a user-defined type that groups together zero or more fields of arbitrary types. Here's an example of a simple struct definition in Go:
```go
type Person struct {
    Name string
    Age  int
}
```
In this example, we define a struct `Person` with two fields `Name` and `Age` of types `string` and `int` respectively. Structs can also be nested within each other, allowing for more complex data structures to be created.

### Interfaces
An interface in Go is a collection of method signatures that a type can implement. Here's an example of an interface definition:
```go
type Shape interface {
    Area() float64
    Perimeter() float64
}
```
In this example, we define an interface `Shape` with two methods `Area()` and `Perimeter()`, both of which return a `float64`. Any type that implements these two methods implicitly satisfies the `Shape` interface.

### Example: Shapes
Let's see how structs and interfaces can be used together in a practical example. We'll define a `Circle` struct and a `Rectangle` struct, both of which implement the `Shape` interface:
```go
type Circle struct {
    Radius float64
}

func (c Circle) Area() float64 {
    return math.Pi * c.Radius * c.Radius
}

func (c Circle) Perimeter() float64 {
    return 2 * math.Pi * c.Radius
}
```
```go
type Rectangle struct {
    Width  float64
    Height float64
}

func (r Rectangle) Area() float64 {
    return r.Width * r.Height
}

func (r Rectangle) Perimeter() float64 {
    return 2 * (r.Width + r.Height)
}
```
Both `Circle` and `Rectangle` structs implement the `Shape` interface by providing their respective implementations for the `Area()` and `Perimeter()` methods.

### Conclusion
Structs and interfaces are powerful features in Go that enable the creation of complex data structures and promote code reusability. By using structs to group related data and interfaces to define common behavior, Go allows for flexible and maintainable code. Be sure to leverage these concepts in your Go programs to write more efficient and organized code.