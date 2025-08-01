---
description: Learn how JavaScript brings interactivity and logic to webpages.
---

# 524 JavaScript in front-end web development

### Overview

In this topic, we explore how JavaScript is used to make webpages interactive and dynamic. Students are introduced to basic programming structures, event handling, and how JavaScript interacts with HTML elements through the Document Object Model (DOM). JavaScript is a core technology in front-end web development and is essential for building modern, user-responsive applications.

### Targets

In this topic, students learn to:

* Explain the role of JavaScript in the front-end of web applications
* Identify how JavaScript interacts with the DOM to change page content
* Use basic syntax to define variables, functions, and conditions
* Respond to user events such as clicks and keypresses
* Understand the difference between HTML, CSS, and JavaScript roles

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Designing web applications**

* Model elements that form a web development system\
  – client-side (front-end) web programming

</details>

### What is JavaScript?

**JavaScript** is a scripting language that runs in the browser and adds interactivity to webpages. While HTML defines structure and CSS defines style, JavaScript enables behaviour—like toggling menus, submitting forms, displaying alerts, or changing content without reloading the page.

JavaScript code can be written:

* Inline within an HTML file
* Inside a `<script>` tag in the HTML document
* As an external `.js` file linked with `<script src="...">`

### Example: JavaScript in action

```html
<button onclick="sayHello()">Click me</button>

<script>
  function sayHello() {
    alert("Hello, world!");
  }
</script>
```

When the button is clicked, the browser runs the `sayHello()` function, displaying an alert.

### How JavaScript interacts with the DOM

The **Document Object Model (DOM)** represents the structure of a webpage. JavaScript can use the DOM to:

* Find elements (`document.querySelector`)
* Change content (`element.textContent`)
* Update styles (`element.style`)
* Add or remove classes (`element.classList.add`)

This makes the webpage dynamic and responsive to input.

### Basic building blocks of JavaScript

* **Variables** store values (`let count = 0;`)
* **Functions** group instructions (`function greet() { ... }`)
* **Events** trigger code (`button.addEventListener("click", runCode);`)
* **Conditional statements** control logic (`if`, `else`)
* **Loops** repeat tasks (`for`, `while`)

These programming fundamentals are shared with other languages and form the basis of further front-end development.

### Summary

JavaScript brings HTML and CSS to life by enabling interactivity and behaviour. It allows developers to build dynamic, event-driven webpages that respond to user actions. JavaScript is an essential part of the front-end stack and a foundational skill for web developers.
