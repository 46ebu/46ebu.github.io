---
title: "[Javascript] Working with Forms and Input Validation"
author: 46ebu
date: 2024-03-15 22:06:06 +0900
categories: [Javascript]
tags: [Javascript]
render_with_liquid: false
---

![Intro](/assets/img/post/javascript.png)
### Introduction
Working with forms and input validation in JavaScript is essential for creating interactive and user-friendly web applications. In this blog post, we will explore the basics of handling forms and ensuring that user input is valid before processing it. 

### HTML Form
When working with forms in HTML, we use the <form> element to create a structure for collecting user input. Each form input field is defined using <input> elements with different types such as text, email, password, etc. Additionally, we can include buttons like submit and reset within the form.

### Using JavaScript for Input Validation
JavaScript allows us to validate user input before submitting the form to the server. By accessing the form element and its input fields, we can add event listeners to check for valid input based on specific criteria. For example, we can check if an email input field contains a valid email address using regular expressions.

### Example Code 1: Basic Form Validation
```javascript
const form = document.querySelector('form');
const emailInput = document.querySelector('#email');

form.addEventListener('submit', function(event) {
  if (!isValidEmail(emailInput.value)) {
    alert('Please enter a valid email address');
    event.preventDefault();
  }
});

function isValidEmail(email) {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
}
```

In this code snippet, we listen for the form submission event and check if the email input field contains a valid email address using a regular expression pattern.

### Example Code 2: Password Matching Validation
```javascript
const passwordInput = document.querySelector('#password');
const confirmInput = document.querySelector('#confirm-password');

confirmInput.addEventListener('input', function() {
  if (confirmInput.value !== passwordInput.value) {
    confirmInput.setCustomValidity('Passwords do not match');
  } else {
    confirmInput.setCustomValidity('');
  }
});
```

Here, we compare the value of the confirmation password input field with the original password input field to ensure they match before submitting the form.

### Example Code 3: Dynamic Input Validation
```javascript
const nameInput = document.querySelector('#name');

nameInput.addEventListener('input', function() {
  if (nameInput.value.length < 3) {
    nameInput.setCustomValidity('Name must be at least 3 characters');
  } else {
    nameInput.setCustomValidity('');
  }
});
```

This code snippet demonstrates dynamic input validation by checking the length of the name input field in real-time as the user types.

### Conclusion
By incorporating input validation with JavaScript, we can enhance the user experience by ensuring that only valid data is submitted through forms. From basic email validation to more complex password matching, JavaScript provides a powerful toolset for creating robust form validation mechanisms.