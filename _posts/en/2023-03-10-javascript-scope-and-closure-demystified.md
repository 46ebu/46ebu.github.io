---
title: "[Javascript] Scope and Closure Demystified"
author: 46ebu
date: 2023-03-10 00:14:46 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-scope-and-closure-demystified
---

![Intro](/assets/img/post/javascript.png)
### Scope in Javascript
In Javascript, scope refers to the visibility of variables. There are two types of scope in Javascript: global scope and local scope. Global scope refers to variables that are accessible throughout the entire program, while local scope refers to variables that are only accessible within a specific function or block of code. The scope of a variable is determined by where it is declared.

### Local Scope Example
```javascript
function myFunction() {
  var localVar = "I am a local variable";
  console.log(localVar);
}

myFunction();
console.log(localVar); // This will result in an error
```
In this example, the variable `localVar` is declared within the `myFunction` function, so it is only accessible within that function. Trying to access `localVar` outside of the function will result in a reference error.

### Global Scope Example
```javascript
var globalVar = "I am a global variable";

function myFunction() {
  console.log(globalVar);
}

myFunction();
console.log(globalVar);
```
In this example, the variable `globalVar` is declared outside of any function, so it is accessible throughout the entire program. It can be accessed both inside and outside of the `myFunction` function.

### Closures in Javascript
A closure is a combination of a function bundled together with references to its surrounding state (the lexical environment). Closures allow functions to access variables from their outer scope even after the outer function has finished executing.

### Closure Example
```javascript
function outerFunction() {
  var outerVar = "I am an outer variable";

  function innerFunction() {
    console.log(outerVar);
  }

  return innerFunction;
}

var closure = outerFunction();
closure();
```
In this example, the `innerFunction` has access to the `outerVar` variable even though it is declared in the `outerFunction` and the `outerFunction` has already finished executing. This is because the `innerFunction` forms a closure over the `outerVar` variable.

### Conclusion
Understanding scope and closure in Javascript is crucial for writing efficient and bug-free code. Properly managing scope helps prevent variable conflicts and unintended side effects, while closures allow for more flexible and modular code design. By mastering these concepts, developers can create more robust and maintainable Javascript applications.