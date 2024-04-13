---
title: "[javascript] json read/write/update method (code example and explanation)"
author: 46ebu
date: 2024-04-13 00:43:43 +0000
categories: [javascript]
tags: [javascript]
render_with_liquid: false
---

![Intro](/assets/img/post/javascript.png)
### Introduction
JSON (JavaScript Object Notation) is a lightweight data-interchange format that is easy for humans to read and write and easy for machines to parse and generate. In JavaScript, JSON is commonly used for storing and exchanging data. In this blog post, we will explore how to read, write, and update JSON data using JavaScript.

### Reading JSON Data
To read JSON data in JavaScript, you can use the `JSON.parse()` method. This method takes a JSON string as a parameter and converts it into a JavaScript object. Here is an example code snippet:

```javascript
const jsonString = '{"name": "John Doe", "age": 30}';
const jsonObject = JSON.parse(jsonString);
console.log(jsonObject);
```

Output:
```javascript
{ name: 'John Doe', age: 30 }
```

### Writing JSON Data
To write JSON data in JavaScript, you can use the `JSON.stringify()` method. This method takes a JavaScript object as a parameter and converts it into a JSON string. Here is an example code snippet:

```javascript
const jsonObject = { name: 'Jane Smith', age: 25 };
const jsonString = JSON.stringify(jsonObject);
console.log(jsonString);
```

Output:
```javascript
{"name":"Jane Smith","age":25}
```

### Updating JSON Data
To update JSON data in JavaScript, you can first read the JSON data, modify the JavaScript object, and then convert it back to a JSON string. Here is an example code snippet:

```javascript
const jsonString = '{"name": "Alice Brown", "age": 35}';
const jsonObject = JSON.parse(jsonString);
jsonObject.name = 'Emily Green';
const updatedJsonString = JSON.stringify(jsonObject);
console.log(updatedJsonString);
```

Output:
```javascript
{"name":"Emily Green","age":35}
```

### Conclusion
In this blog post, we have explored how to read, write, and update JSON data in JavaScript using the `JSON.parse()` and `JSON.stringify()` methods. Understanding these methods is essential for working with JSON data in JavaScript applications. The examples provided demonstrate how to manipulate JSON data efficiently. These methods are available in all modern versions of JavaScript, making them suitable for use in a wide range of projects. Next time you need to handle JSON data in JavaScript, give these methods a try for a seamless data management experience.