---
title: "[GO] Exploring Structs and Interfaces"
author: 46ebu
date: 2023-04-25 12:57:30 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-exploring-structs-and-interfaces
---

![Intro](/assets/img/post/go.png)
### Introduction
In Go, structs and interfaces are fundamental concepts that play a significant role in creating scalable and modular code. Structs are data structures that can hold multiple fields of different data types, while interfaces define a set of methods that a type must implement. Understanding how to effectively use structs and interfaces can greatly enhance the design and flexibility of your Go programs.

### Structs
Structs in Go are collections of fields that can be of any type, including other structs or interfaces. They are defined using the `type` keyword followed by the `struct` keyword and a list of fields enclosed in curly braces. Here is an example of a simple struct definition in Go:

```go
type Person struct {
    Name string
    Age  int
}
```

In this example, we have defined a struct called `Person` with two fields: `Name` of type `string` and `Age` of type `int`. We can create an instance of this struct by initializing it with values for each field:

```go
person := Person{Name: "Alice", Age: 30}
fmt.Println(person.Name) // Output: Alice
fmt.Println(person.Age) // Output: 30
```

### Interfaces
Interfaces in Go are a powerful way to define behavior without specifying implementation. They are defined using the `type` keyword followed by the `interface` keyword and a list of method signatures. Any type that implements all the methods defined in the interface is said to satisfy that interface. Here is an example of an interface in Go:

```go
type Shape interface {
    Area() float64
}

```

In this example, we have defined an interface called `Shape` with a single method `Area` that returns a `float64`. Any type that implements the `Area()` method can satisfy the `Shape` interface. Here is an example of a struct that implements the `Shape` interface:

```go
type Circle struct {
    Radius float64
}

func (c Circle) Area() float64 {
    return math.Pi * c.Radius * c.Radius
}
```

In this example, the `Circle` struct implements the `Area()` method, making it compatible with the `Shape` interface. We can create an instance of the `Circle` struct and use it as a `Shape`:

```go
circle := Circle{Radius: 5}
var shape Shape
shape = circle
fmt.Println(shape.Area()) // Output: 78.53981633974483

```

### Conclusion
Structs and interfaces are powerful concepts in Go that allow developers to write clean, modular, and scalable code. By utilizing structs to define data structures and interfaces to define behavior, you can create flexible and efficient programs. Understanding how to effectively use structs and interfaces is essential for any Go developer looking to write high-quality code.