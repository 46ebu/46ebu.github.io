---
title: "[GO] Introduction to WebSockets in Go"
author: 46ebu
date: 2023-05-24 16:28:00 
categories: [GO]
tags: [GO]
render_with_liquid: false
lang: en
permalink: /go-introduction-to-websockets-in-go
---

![Intro](/assets/img/post/go.png)
### What are WebSockets?

WebSockets provide a full-duplex communication channel over a single, long-lived connection between a client and server. This allows for real-time, bi-directional communication on the web, making it ideal for applications that require instant updates or notifications.

### Implementing WebSockets in Go

In Go, the standard library provides a built-in package for working with WebSockets called `github.com/gorilla/websocket`. To use this package, you first need to install it using `go get`:

```go
go get github.com/gorilla/websocket
```

### Creating a WebSocket Server

To create a WebSocket server in Go, you first need to establish an HTTP server using the `net/http` package. Then, you can upgrade the HTTP connection to a WebSocket connection using the `Upgrade` method from the `websocket` package:

```go
package main

import (
	"fmt"
	"net/http"

	"github.com/gorilla/websocket"
)

var upgrader = websocket.Upgrader{
	CheckOrigin: func(r *http.Request) bool {
		return true
	},
}

func handler(w http.ResponseWriter, r *http.Request) {
	conn, err := upgrader.Upgrade(w, r, nil)
	if err != nil {
		fmt.Println(err)
		return
	}
	defer conn.Close()
	// WebSocket connection logic here
}

func main() {
	http.HandleFunc("/", handler)
	http.ListenAndServe(":8080", nil)
}
```

### Creating a WebSocket Client

On the client side, you can establish a WebSocket connection using the `websocket.Dial` function:

```go
package main

import (
	"fmt"
	"log"
	"net/url"

	"github.com/gorilla/websocket"
)

func main() {
	u := url.URL{Scheme: "ws", Host: "localhost:8080", Path: "/"}
	c, _, err := websocket.DefaultDialer.Dial(u.String(), nil)
	if err != nil {
		log.Fatal("dial:", err)
	}
	defer c.Close()
	// WebSocket client logic here
}
```

### Conclusion

WebSockets offer a powerful way to enable real-time communication in web applications using Go. By implementing WebSocket servers and clients, you can create interactive, dynamic applications that push updates to clients instantly. The `github.com/gorilla/websocket` package simplifies the process of working with WebSockets in Go, allowing you to focus on building innovative web applications.