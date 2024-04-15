---
title: "[javascript] 3 ways to reverse string"
author: 46ebu
date: 2024-04-15 07:36:23 +0000
categories: [javascript]
tags: [javascript]
render_with_liquid: false
---

![Intro](/assets/img/post/javascript.png)
### Introduction
Reversing a string is a common task in programming, and JavaScript offers several ways to achieve this. In this blog post, we will explore three different methods to reverse a string in JavaScript.

### Method 1: Using the split(), reverse(), and join() methods
```javascript
const str = "hello";
const reversedStr = str.split("").reverse().join("");
console.log(reversedStr);
```
This method involves splitting the string into an array of characters using the split() method, reversing the order of the elements in the array using the reverse() method, and then joining the elements back together into a string using the join() method. The output for the above code would be "olleh".

### Method 2: Using a for loop
```javascript
const str = "hello";
let reversedStr = "";
for (let i = str.length - 1; i >= 0; i--) {
  reversedStr += str[i];
}
console.log(reversedStr);
```
In this method, we iterate over the characters of the input string in reverse order using a for loop and concatenate each character to a new string. The output for the above code would also be "olleh".

### Method 3: Using the reduce() method
```javascript
const str = "hello";
const reversedStr = str.split("").reduce((acc, char) => char + acc, "");
console.log(reversedStr);
```
This method utilizes the reduce() method to iterate over each character in the input string and build up a new string by prepending each character to the accumulated result (initially an empty string). The output for the above code would once again be "olleh".

### Conclusion
In this blog post, we explored three different methods to reverse a string in JavaScript. Each method offers a unique approach to achieving the desired result, providing flexibility based on the specific requirements of the task at hand. Whether using the split(), reverse(), and join() methods, a for loop, or the reduce() method, developers have multiple options to choose from when it comes to reversing a string in JavaScript.