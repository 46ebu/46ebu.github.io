---
title: "[Javascript] Exploring Web APIs and AJAX"
author: 46ebu
date: 2021-02-23 09:07:20 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-exploring-web-apis-and-ajax
---

![Intro](/assets/img/post/javascript.png)
### What are Web APIs and AJAX?

Web APIs (Application Programming Interfaces) are interfaces that allow different software systems to communicate with each other. In web development, Web APIs are commonly used to interact with external services or applications. AJAX (Asynchronous JavaScript and XML) is a technique used to make asynchronous requests to a server without reloading the entire webpage. This allows for a smoother user experience as data can be loaded in the background without disrupting the user's current interaction with the page.

### How to use Web APIs in Javascript

In Javascript, we can make HTTP requests to a Web API using the `fetch()` function. This function returns a Promise that resolves to the Response to that request, allowing us to handle the data returned by the API. Here is an example code snippet demonstrating how to fetch data from a Web API using `fetch()`:

```javascript
fetch('https://api.example.com/data')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error('Error fetching data:', error));
```

In this code snippet, we use the `fetch` function to make a GET request to the specified API endpoint. We then chain the `.then()` method to handle the response by parsing it as JSON. Finally, we log the data to the console or handle any errors using the `.catch()` method.

### Using AJAX in Javascript

To make an AJAX request in Javascript, we can use the `XMLHttpRequest` object. This object allows us to send HTTP requests to a server and handle the response. Here is a basic example of how to make an AJAX request using `XMLHttpRequest`:

```javascript
let xhr = new XMLHttpRequest();
xhr.open('GET', 'https://api.example.com/data', true);

xhr.onload = function() {
  if (xhr.status >= 200 && xhr.status < 300) {
    console.log(JSON.parse(xhr.responseText));
  } else {
    console.error('Failed to fetch data:', xhr.statusText);
  }
};

xhr.onerror = function () {
  console.error('Failed to fetch data');
};

xhr.send();
```

In this code snippet, we create a new `XMLHttpRequest` object and specify the type of request (GET) and the URL of the API endpoint. We then define an `onload` event handler to process the response data and handle any errors using the `onerror` event handler.

### Versions and Browser Support

Web APIs and AJAX have been around for a long time and are supported by all modern browsers. The `fetch()` function is a newer addition to the Javascript language and is supported in most modern browsers, including Chrome, Firefox, and Edge. Older browsers may require a polyfill to use the `fetch()` function. `XMLHttpRequest` is a more traditional way of making AJAX requests and is supported by all browsers.

In conclusion, Web APIs and AJAX are powerful tools in a web developer's toolkit for making asynchronous requests to external services and improving the user experience. By using `fetch()` and `XMLHttpRequest`, developers can interact with Web APIs and retrieve data dynamically without reloading the entire webpage.