---
title: "[Javascript] Introduction to WebSockets and Real-Time Communication"
author: 46ebu
date: 2021-12-25 19:01:40 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-introduction-to-websockets-and-realtime-communication
---

![Intro](/assets/img/post/javascript.png)
### Introduction
WebSockets are a powerful technology that enables bidirectional communication between a web client and a server over a single, long-lived connection. This allows for real-time data transfer between the two parties, making it ideal for applications that require instant updates, such as online gaming, chat applications, and collaborative editing tools.

### How WebSockets Work
WebSockets use the WebSocket protocol, which is built on top of the TCP protocol. Unlike traditional HTTP requests that are stateless and require the client to initiate communication, WebSockets provide a persistent connection that both the client and server can use to send data back and forth at any time.

To establish a WebSocket connection from the client side in JavaScript, you can use the WebSocket API, which is supported by most modern web browsers. Here's an example of how you can create a WebSocket object and connect to a server:

```javascript
const socket = new WebSocket("ws://localhost:3000");

socket.onopen = function() {
  console.log("Connection opened");
};

socket.onmessage = function(event) {
  console.log("Message received:", event.data);
};

socket.onclose = function() {
  console.log("Connection closed");
};
```

### Real-Time Communication
Once the WebSocket connection is established, both the client and server can send messages to each other in real-time. For example, in a chat application, when a user sends a message, the client can send that message to the server, which then broadcasts it to all connected clients.

Here's an example of how you can send a message from the client to the server using the WebSocket connection:

```javascript
const message = "Hello, server!";
socket.send(message);
```

And here's an example of how the server can broadcast a message to all connected clients:

```javascript
// Inside the server logic
wss.on("connection", function(socket) {
  socket.on("message", function(message) {
    wss.clients.forEach(function(client) {
      client.send(message);
    });
  });
});
```

### Conclusion
WebSockets provide a seamless way to enable real-time communication between a web client and server, making it a powerful tool for building interactive and dynamic web applications. By utilizing the WebSocket API in JavaScript, developers can create applications that can push data to clients instantly, creating a more engaging user experience.