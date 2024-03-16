---
title: "[GO] A Deep Dive into Go Generics"
author: 46ebu
date: 2023-09-03 07:50:00 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-a-deep-dive-into-go-generics
---

![Intro](/assets/img/post/go.png)
### Introduction
Generics is an upcoming feature in Go that has been highly anticipated by the community. It aims to provide a way to write functions and data structures that can operate on any type. This would eliminate the need for writing boilerplate code for different types and promote code reusability.

### Syntax
The syntax for defining generic functions in Go looks like this:
```go
func PrintSlice[T any](s []T) {
    for _, elem := range s {
        fmt.Println(elem)
    }
}
```
Here, `T any` indicates that `PrintSlice` is a generic function that can accept any type.

### Example Codes
Let's take a look at three examples to better understand how generics work in Go:

1. Generic Slice Reversal Function:
```go
func Reverse[T any](s []T) []T {
    reversed := make([]T, len(s))
    for i := range s {
        reversed[len(s)-1-i] = s[i]
    }
    return reversed
}
```

2. Generic Map Function:
```go
func Map[T any, U any](s []T, f func(T) U) []U {
    mapped := make([]U, len(s))
    for i, elem := range s {
        mapped[i] = f(elem)
    }
    return mapped
}
```

3. Generic Stack Data Structure:
```go
type Stack[T any] struct {
    items []T
}

func (s *Stack[T]) Push(item T) {
    s.items = append(s.items, item)
}

func (s *Stack[T]) Pop() T {
    item := s.items[len(s.items)-1]
    s.items = s.items[:len(s.items)-1]
    return item
}
```

### Applicable Versions
Go generics are currently in development and are expected to be released in Go 1.18. However, you can try out the experimental generics using the `-gcflags="all=-G=3` flag in Go 1.17.

In conclusion, Go generics promise to make Go code more concise and readable by allowing developers to write generic functions and data structures that can operate on any type. While the feature is not yet stable, it is definitely something to look forward to in future Go releases.