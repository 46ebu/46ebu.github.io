---
title: "[GO] Concurrency in Go: Goroutines and Channels"
author: 46ebu
date: 2023-04-04 15:38:27 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-concurrency-in-go-goroutines-and-channels
---

![Intro](/assets/img/post/go.png)
### Introduction
Concurrency in programming allows us to execute multiple tasks simultaneously, improving efficiency and performance. In Go, concurrency is achieved through goroutines and channels. Goroutines are lightweight threads managed by the Go runtime, while channels are used to communicate and synchronize data between goroutines.

### Goroutines
In Go, a goroutine is created using the `go` keyword followed by a function call. This function will then be executed concurrently with the main program. Goroutines are lightweight, enabling developers to create thousands of them without incurring much overhead.

```go
func main() {
    go hello()
    time.Sleep(1 * time.Second)
}

func hello() {
    fmt.Println("Hello from goroutine!")
}
```

In the example above, the `hello` function is executed concurrently in a goroutine while the main program continues running. This allows for parallelism in the code execution.

### Channels
Channels in Go are used to communicate and synchronize data between goroutines. They provide a way for goroutines to send and receive data safely without the need for explicit locking mechanisms. Channels can be either unbuffered or buffered.

```go
func main() {
    ch := make(chan int)

    go func() {
        ch <- 42
    }()

    value := <-ch
    fmt.Println(value)
}
```

In this example, a channel `ch` of type `int` is created using the `make` function. A goroutine is then started to send the value 42 into the channel, which is then received and printed in the main program.

### Select Statement
The `select` statement in Go allows for non-blocking communication with multiple channels. It waits for one of the cases to be ready and then executes the corresponding block of code. This is useful for handling multiple channels concurrently.

```go
func main() {
    ch1 := make(chan string)
    ch2 := make(chan string)

    go func() {
        ch1 <- "hello"
    }()
    
    go func() {
        ch2 <- "world"
    }()

    select {
    case msg1 := <-ch1:
        fmt.Println(msg1)
    case msg2 := <-ch2:
        fmt.Println(msg2)
    }
}
```

In this code snippet, two goroutines are started to send messages into two different channels. The `select` statement then waits for either channel to be ready and prints the corresponding message.

Overall, goroutines and channels in Go provide a powerful and efficient way to implement concurrency in your applications. By utilizing these features, developers can take advantage of parallelism and improve the performance of their programs. Go has built-in support for concurrency with Goroutines and Channels, making it a great language for concurrent programming tasks.