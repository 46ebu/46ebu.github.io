---
title: "[Javascript] Local Storage and Session Storage"
author: 46ebu
date: 2020-08-22 03:14:07 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-local-storage-and-session-storage
---

![Intro](/assets/img/post/javascript.png)
### Introduction
Local Storage and Session Storage in Javascript are two ways to store data on the client-side browser. They provide a way to keep information stored even when the browser is closed and reopened, making them useful for saving user preferences, session data, and more.

### Local Storage
Local Storage is a type of web storage that allows you to store data with no expiration date. This means the data will persist even when the browser is closed and reopened. You can store up to 5MB of data in Local Storage, which is significantly more than the 4KB limit of cookies.

To set an item in Local Storage, you can use the `localStorage.setItem()` method. Here's an example:

```javascript
localStorage.setItem('username', 'john_doe');
```

To retrieve an item from Local Storage, you can use the `localStorage.getItem()` method. Here's an example:

```javascript
var username = localStorage.getItem('username');
```

To remove an item from Local Storage, you can use the `localStorage.removeItem()` method. Here's an example:

```javascript
localStorage.removeItem('username');
```

### Session Storage
Session Storage is similar to Local Storage, but the data stored in Session Storage is only available for the duration of the page session. Once the user closes the browser tab or window, the data is cleared. This makes Session Storage useful for storing temporary data that is only needed for a short period of time.

To set an item in Session Storage, you can use the `sessionStorage.setItem()` method. Here's an example:

```javascript
sessionStorage.setItem('theme', 'dark');
```

To retrieve an item from Session Storage, you can use the `sessionStorage.getItem()` method. Here's an example:

```javascript
var theme = sessionStorage.getItem('theme');
```

To remove an item from Session Storage, you can use the `sessionStorage.removeItem()` method. Here's an example:

```javascript
sessionStorage.removeItem('theme');
```

### Conclusion
In conclusion, Local Storage and Session Storage are powerful tools in web development for storing data on the client-side browser. They provide a convenient way to save and access information, making them essential for building interactive web applications. By understanding how to use Local Storage and Session Storage effectively, developers can enhance the user experience and create more dynamic websites.