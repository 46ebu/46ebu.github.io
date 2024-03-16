---
title: "[JavaScript] Introduction to JavaScript"
author: 46ebu
date: 2022-02-12 02:48:45 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-introduction-to-javascript
---

![Intro](/assets/img/post/javascript.png)
### What is JavaScript?

JavaScript is a high-level, interpreted programming language that is commonly used in web development to add interactivity and dynamic behavior to websites. It is a versatile language that can be used both on the client-side (in the browser) and on the server-side (with Node.js). JavaScript is widely supported by all modern web browsers, making it one of the most popular programming languages in the world.

### Syntax and Basic Structure

JavaScript code is typically embedded directly into HTML files using `<script>` tags. It can also be included in external JavaScript files with the .js extension. JavaScript is a case-sensitive language and uses curly braces `{}` to create blocks of code. Statements in JavaScript are terminated by semicolons `;`.

Here is a simple example of a Hello World program in JavaScript:

```javascript
<script>
  document.write("Hello, World!");
</script>
```

### Variables and Data Types

JavaScript is a dynamically typed language, meaning that variables do not have a specific data type assigned to them. Instead, the data type is determined at runtime based on the value assigned to the variable. JavaScript supports various data types, including numbers, strings, booleans, arrays, objects, and functions.

Here is an example of declaring and initializing variables in JavaScript:

```javascript
<script>
  var num = 10;
  var str = "Hello, World!";
  var bool = true;

  document.write(num + "<br>");
  document.write(str + "<br>");
  document.write(bool);
</script>
```

### Functions and Control Structures

Functions are a fundamental feature of JavaScript, allowing you to encapsulate reusable blocks of code. Functions can take parameters and return values, making them versatile and powerful. JavaScript also supports various control structures, including if statements, switch statements, for loops, while loops, and more.

Here is an example of a simple function in JavaScript:

```javascript
<script>
  function addNumbers(a, b) {
    return a + b;
  }

  var result = addNumbers(5, 3);
  document.write("The sum is: " + result);
</script>
```

JavaScript continues to evolve with new features and improvements, with the latest version being ECMAScript 2021. By mastering the basics of JavaScript, you can build dynamic and interactive web applications that delight users and provide a seamless user experience.