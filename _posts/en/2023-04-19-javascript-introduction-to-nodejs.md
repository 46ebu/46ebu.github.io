---
title: "[Javascript] Introduction to Node.js"
author: 46ebu
date: 2023-04-19 16:36:49 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-introduction-to-nodejs
---

![Intro](/assets/img/post/javascript.png)
### What is Node.js?
Node.js is an open-source, runtime environment that allows JavaScript to run on the server-side. It uses the V8 JavaScript engine from Google Chrome to execute code outside of a browser. This allows developers to use JavaScript to build scalable network applications.

### Installing Node.js
Before getting started with Node.js, you need to install it on your machine. You can download and install Node.js from the official website or use a package manager like npm to install it. Once installed, you can check the version of Node.js using the terminal with the command `node -v`.

### Getting Started with Node.js
To create a basic Node.js application, you can simply create a new JavaScript file with a .js extension and write your code. You can run the file using the command `node filename.js` in the terminal. Here is a simple example of a Node.js program:
```javascript
// hello.js
console.log('Hello, Node.js!');
```

### Using Modules in Node.js
Node.js has a built-in module system that allows you to organize your code into reusable modules. You can create a module by defining functions, variables, or classes in a separate file and then exporting them using `module.exports`. Here is an example of creating and using a module in Node.js:
```javascript
// math.js
module.exports.add = function(a, b) {
    return a + b;
};

// app.js
const math = require('./math');
console.log(math.add(2, 3)); // Output: 5
```

### Asynchronous Programming in Node.js
Node.js is known for its non-blocking, asynchronous nature, which allows it to handle multiple requests simultaneously without blocking the execution of other code. You can use callbacks, promises, or async/await to handle asynchronous operations in Node.js. Here is an example using callbacks to read a file asynchronously:
```javascript
const fs = require('fs');
fs.readFile('example.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
});
```

### Conclusion
Node.js is a powerful runtime environment for running JavaScript on the server-side. It provides a wide range of modules and libraries to help you build efficient and scalable applications. By learning the basics of Node.js, you can take advantage of its features to create robust backend services and applications.