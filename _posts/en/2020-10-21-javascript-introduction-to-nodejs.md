---
title: "[Javascript] Introduction to Node.js"
author: 46ebu
date: 2020-10-21 17:43:25 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-introduction-to-nodejs
---

![Intro](/assets/img/post/javascript.png)
### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript outside the browser. It uses the V8 JavaScript engine, the same engine that powers Google Chrome, to execute code. Node.js provides an event-driven, non-blocking I/O model that makes it lightweight and efficient for building scalable network applications.

### Installing Node.js

To start using Node.js, you need to install it on your machine. You can download the installer from the Node.js website and follow the installation instructions for your operating system. Once installed, you can check the version of Node.js installed by running `node -v` in the terminal.

### Getting Started with Node.js

One of the key features of Node.js is the `npm` (Node Package Manager) that comes bundled with it. `npm` allows you to easily install and manage third-party libraries and packages for your Node.js projects. To create a new Node.js project, you can run `npm init` in the terminal and follow the prompts to set up your project.

### Example Code in Node.js

1. **Hello World**
   
   ```javascript
   // hello.js
   console.log("Hello, World!");
   ```
   
   To run this script, save the code in a file named `hello.js` and run `node hello.js` in the terminal. You should see the output "Hello, World!" displayed.

2. **Reading a File**
   
   ```javascript
   // readfile.js
   const fs = require('fs');
   
   fs.readFile('example.txt', 'utf8', (err, data) => {
       if (err) throw err;
       console.log(data);
   });
   ```

   This script reads the contents of a file named `example.txt` and logs it to the console.

3. **Creating a Simple HTTP Server**
   
   ```javascript
   // server.js
   const http = require('http');
   
   const server = http.createServer((req, res) => {
       res.writeHead(200, {'Content-Type': 'text/plain'});
       res.end('Hello, World!\n');
   });
   
   server.listen(3000, '127.0.0.1', () => {
       console.log('Server running at http://127.0.0.1:3000/');
   });
   ```

   This script creates a basic HTTP server that listens on port 3000 and responds with "Hello, World!" to incoming requests.

### Conclusion

Node.js is a powerful tool for building server-side applications using JavaScript. Its asynchronous, event-driven architecture makes it well-suited for handling I/O-heavy tasks and building real-time applications. With its vast ecosystem of libraries and packages available through `npm`, Node.js has become a popular choice for developers looking to build scalable and efficient web applications.