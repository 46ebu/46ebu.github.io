---
title: "[GO] Introduction to WebSockets in Go"
author: 46ebu
date: 2024-03-15 19:43:27 +0900
categories: [GO]
tags: [GO]
render_with_liquid: false
---

![Intro](/assets/img/post/go.png)
### What are WebSockets?

WebSockets are a protocol that provides full-duplex communication channels over a single TCP connection. This allows for real-time communication between clients and servers. In Go, you can implement WebSockets using the "github.com/gorilla/websocket" package.

### Installing Gorilla WebSocket package

To use WebSockets in Go, you first need to install the Gorilla WebSocket package. You can do so using the following go get command:

```go
go get github.com/gorilla/websocket
```

### Creating a WebSocket server in Go

Here's a simple example of how you can create a WebSocket server in Go:

```go
package main

import (
	"net/http"

	"github.com/gorilla/websocket"
)

var upgrader = websocket.Upgrader{
	CheckOrigin: func(r *http.Request) bool {
		return true
	},
}

func handleConnections(w http.ResponseWriter, r *http.Request) {
	conn, _ := upgrader.Upgrade(w, r, nil)
	defer conn.Close()
}

func main() {
	http.HandleFunc("/", handleConnections)
	http.ListenAndServe(":8080", nil)
}
```

In the above code, we create an HTTP server and upgrade the HTTP connection to a WebSocket connection in the handleConnections function.

### Creating a WebSocket client in Go

Here's an example of how you can create a WebSocket client in Go:

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
}
```

In the above code, we create a WebSocket client that connects to the WebSocket server running on localhost:8080.

### Conclusion

WebSockets provide a powerful way to implement real-time communication in web applications. With the Gorilla WebSocket package in Go, you can easily create WebSocket servers and clients. By following the examples provided in this post, you can start building real-time applications using WebSockets in Go.

In conclusion, Go provides a robust and efficient way to implement WebSockets in your applications. By using the Gorilla WebSocket package, you can easily create WebSocket servers and clients for real-time communication.