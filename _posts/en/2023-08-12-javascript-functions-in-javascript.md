---
title: "[Javascript] Functions in JavaScript"
author: 46ebu
date: 2023-08-12 20:25:20 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-functions-in-javascript
---

![Intro](/assets/img/post/javascript.png)
### Introduction
Functions in JavaScript are a fundamental concept that allows developers to create reusable blocks of code. In JavaScript, functions are first-class objects, which means they can be passed around as arguments and returned from other functions.

### Function Declaration
In JavaScript, functions can be declared using the `function` keyword followed by the function name and parameters enclosed in parentheses. The body of the function is enclosed in curly braces. Here's an example of a simple function declaration:

```javascript
function greet(name) {
    return "Hello, " + name;
}
```

### Function Expression
Another way to define functions in JavaScript is through function expressions. In function expressions, the function is assigned to a variable. Here's an example of a function expression:

```javascript
const greet = function(name) {
    return "Hello, " + name;
};
```

### Arrow Functions
Arrow functions are a concise way to write functions in JavaScript. They were introduced in ES6 (ECMAScript 2015) and provide a more compact syntax compared to traditional function expressions. Here's an example of an arrow function:

```javascript
const greet = (name) => {
    return "Hello, " + name;
};
```

### Higher-Order Functions
Functions in JavaScript are first-class citizens, which means they can be passed as arguments to other functions. Functions that operate on other functions, either by taking them as arguments or by returning them, are known as higher-order functions. Here's an example of a higher-order function that takes another function as an argument:

```javascript
function operateOnNumber(num, operation) {
    return operation(num);
}

function square(num) {
    return num * num;
}

console.log(operateOnNumber(3, square)); // Output: 9
```

### Callback Functions
Callback functions are functions that are passed as arguments to other functions and are executed after a certain task has been completed. They are commonly used in asynchronous programming and event handling. Here's an example of using a callback function:

```javascript
function fetchData(callback) {
    setTimeout(() => {
        const data = "Data fetched successfully";
        callback(data);
    }, 2000);
}

function displayData(data) {
    console.log(data);
}

fetchData(displayData); // Output: Data fetched successfully

```

### Conclusion
Functions in JavaScript are a versatile and powerful feature that allows developers to write modular and efficient code. Understanding the different ways to define and use functions, such as function declarations, function expressions, arrow functions, higher-order functions, and callback functions, is crucial for mastering JavaScript development.