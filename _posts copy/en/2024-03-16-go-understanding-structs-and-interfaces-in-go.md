---
title: "[GO] Understanding Structs and Interfaces in Go"
author: 46ebu
date: 2024-03-16 15:37:31 +0900
categories: [GO]
tags: [GO]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### Introduction to Structs and Interfaces
In Go, structs are a way to group variables together under a single name while interfaces define a set of method signatures. Structs and interfaces play a crucial role in defining the structure and behavior of Go programs.

### Structs in Go
In Go, a struct is defined using the `type` keyword followed by the name of the struct and a set of fields enclosed in curly braces. Each field has a name and a type. Here's an example of a struct representing a person:

```go
type Person struct {
    Name string
    Age int
}
```

In the above example, we have defined a struct named `Person` with two fields - Name of type string and Age of type int. We can create a new instance of this struct by assigning values to its fields.

### Interfaces in Go
Interfaces in Go are a collection of method signatures. They define the behavior of objects in terms of the methods they implement. Here's an example of an interface named `Shape` with a method called `Area`:

```go
type Shape interface {
    Area() float64
}
```

In the above example, we have defined an interface named `Shape` with a single method `Area` that returns a float64 value. Any type that implements this method can be considered as a `Shape`.

### Example: Using Structs and Interfaces Together
Let's create a struct called `Circle` that implements the `Shape` interface:

```go
type Circle struct {
    Radius float64
}

func (c Circle) Area() float64 {
    return math.Pi * c.Radius * c.Radius
}
```

In this example, we have defined a struct named `Circle` with a field `Radius` of type float64. We then define a method `Area` on the `Circle` struct that calculates the area of the circle using its radius.

### Conclusion
Structs and interfaces are fundamental concepts in Go programming. Structs allow you to group related variables together, while interfaces define the behavior that objects should implement. By understanding and using structs and interfaces effectively, you can write more modular and reusable code in Go.