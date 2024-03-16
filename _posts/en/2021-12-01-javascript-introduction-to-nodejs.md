---
title: "[Javascript] Introduction to Node.js"
author: 46ebu
date: 2021-12-01 17:00:22 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-introduction-to-nodejs
---

![Intro](/assets/img/post/javascript.png)
### What is Node.js?

Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript code outside of a web browser. It uses the V8 JavaScript engine from Chrome to execute code, making it a powerful tool for building server-side applications. Node.js is known for its event-driven, non-blocking I/O model, which allows for efficient handling of a large number of connections.

### Installing Node.js

To get started with Node.js, you first need to install it on your system. You can download the installer from the official Node.js website (https://nodejs.org) and follow the installation instructions for your operating system. Once installed, you can check the version of Node.js using the command `node -v`.

### Creating a Simple Node.js Application

Let's create a simple "Hello World" application using Node.js. Create a new file called `app.js` and add the following code:

```javascript
// Import the http module
const http = require('http');

// Create a server object
http.createServer((req, res) => {
  // Set the response HTTP header with HTTP status code 200 (OK)
  res.writeHead(200, {'Content-Type': 'text/plain'});
  // Send the response body "Hello World"
  res.end('Hello World\n');
}).listen(3000);

console.log('Server running at http://localhost:3000/');
```

In this code, we import the `http` module, create a server object that listens on port 3000, and sends a "Hello World" response to the client when a request is received. You can run this application using the command `node app.js` and access it at `http://localhost:3000/`.

### Working with NPM Packages

Node.js comes with a powerful package manager called NPM (Node Package Manager) that allows you to easily manage and install dependencies for your project. You can install packages using the command `npm install <package-name>`. For example, to install the `express` package, you can run `npm install express`. You can also create a `package.json` file to define the dependencies of your project.

With Node.js, you can build fast and scalable web applications, real-time applications, APIs, and more. It is widely used in web development and has a large ecosystem of libraries and frameworks that make it easy to build robust applications.

### Conclusion

In this blog post, we covered the basics of Node.js, including what it is, how to install it, and how to create a simple application. We also discussed working with NPM packages and the power of Node.js for building server-side applications. Node.js is a versatile tool that has revolutionized the way JavaScript is used in the development of web applications.