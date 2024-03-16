---
title: "[Javascript] Events and Event Handling"
author: 46ebu
date: 2021-07-04 15:23:28 
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
lang: en
permalink: /javascript-events-and-event-handling
---

![Intro](/assets/img/post/javascript.png)
### Introduction
In Javascript, events are actions that occur as a result of user interactions such as clicking a button, hovering over an element, submitting a form, etc. Event handling is the process of writing code that responds to these events. It is a crucial aspect of web development as it allows developers to create interactive and dynamic websites.

### Event Listeners
Event listeners are functions that are triggered when a specific event occurs on an element. They are used to handle events in Javascript. To add an event listener to an element, you can use the `addEventListener` method. Here is an example:

```javascript
const button = document.getElementById('myButton');
button.addEventListener('click', function() {
  console.log('Button clicked!');
});
```

In this example, the `click` event listener is added to the button element with the id `myButton`. When the button is clicked, the function inside the event listener will be executed.

### Event Object
When an event is triggered, an event object is passed to the event handler function. This object contains information about the event such as the type of event, the target element, and any additional data related to the event. You can access this object by passing it as a parameter to the event handler function. Here is an example:

```javascript
const button = document.getElementById('myButton');
button.addEventListener('click', function(event) {
  console.log(event.type);
  console.log(event.target);
});
```

In this example, we are logging the type of event and the target element of the event when the button is clicked.

### Event Propagation
Event propagation refers to the order in which events are triggered on nested elements. There are two phases of event propagation: capturing phase and bubbling phase. In the capturing phase, the event is triggered from the top-level element to the target element. In the bubbling phase, the event is triggered from the target element back up to the top-level element. You can control the propagation of events using the `stopPropagation` method. Here is an example:

```javascript
const parent = document.getElementById('parent');
const child = document.getElementById('child');

parent.addEventListener('click', function() {
  console.log('Parent clicked!');
}, true);

child.addEventListener('click', function(event) {
  event.stopPropagation();
  console.log('Child clicked!');
}, true);
```

In this example, we have two nested elements, a parent and a child. The event listener on the child element stops the event propagation using the `stopPropagation` method, so only the child element's event handler will be executed when it is clicked.

### Conclusion
Events and event handling are essential concepts in Javascript as they allow developers to create interactive and dynamic web applications. By utilizing event listeners, event objects, and event propagation, developers can create responsive and user-friendly websites. It is important to understand these concepts to build robust and engaging web applications.