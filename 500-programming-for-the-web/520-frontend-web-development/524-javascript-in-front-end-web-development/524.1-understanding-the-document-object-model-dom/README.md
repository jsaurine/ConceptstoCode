---
description: >-
  Learn how the Document Object Model (DOM) structures a webpage and how
  JavaScript interacts with it to dynamically modify content, laying the
  foundation for interactive web applications.
---

# 524.1 / Understanding the Document Object Model (DOM)

### TL;DR

The Document Object Model (DOM) is the structured representation of a webpage that browsers create from HTML. JavaScript interacts with the DOM to modify content dynamically, making web pages interactive. The DOM represents HTML elements as a hierarchical tree structure, where JavaScript can dynamically select, modify, and respond to elements.

This topic explains how the DOM works, how browsers construct it, and how JavaScript accesses and manipulates elements. Understanding the DOM is crucial for developing interactive web applications and forms the foundation for JavaScript-driven front-end development.

### Targets

By the end of this lesson, you will be able to

* Explain the role of the DOM in web development and how it represents a webpage.&#x20;
* Describe how the browser constructs the DOM from HTML.&#x20;
* Understand the DOM tree structure and its elements.&#x20;
* Identify different types of nodes in the DOM, including elements, attributes, and text.&#x20;
* Use JavaScript to access and traverse the DOM to find elements dynamically.

{% embed url="https://apollo-academy.slides.com/jbsaurine/5241-document-object-model-dom/embed?token=fg5rwBBZ" %}

### What is the DOM?

The Document Object Model (DOM) is a tree-like representation of a webpage. When a browser loads an HTML file, it parses the content and converts it into a structured model. This allows JavaScript to modify and interact with elements on the page dynamically.

The DOM is hierarchical, representing elements in a parent-child relationship. It is dynamic, allowing JavaScript to update, remove, or add elements to the DOM without reloading the page. It is accessible through JavaScript, with the document object providing methods to interact with the DOM.

### How browsers construct the DOM

When an HTML page loads, the browser follows a sequence of steps.&#x20;

* First, it reads the HTML file and starts parsing its elements.
* Then, it creates the DOM tree, representing elements as objects in a hierarchical structure. It links CSS styles to elements in a separate CSS Object Model (CSSOM).
* The browser then renders the page on the screen by combining the DOM and CSSOM.&#x20;
* Finally, after this process is complete, JavaScript can modify the DOM dynamically.

A basic HTML file consists of elements such as headings, paragraphs, and buttons. When the browser constructs the DOM, it organises these elements into a structured tree. For example, an HTML file with a heading, a paragraph, and a button would have a corresponding DOM representation, where each element is a node in the tree.

This example shows how the browser organises some simple elements in HTML into a tree structure.

{% tabs %}
{% tab title="HTML" %}
```html
<!DOCTYPE html>
<html>
<head><title>My Page</title></head>
<body>
    <h1 id="title">Hello, World!</h1>
    <p>This is a paragraph.</p>
    <button id="changeText">Click Me</button>
</body>
</html>
```
{% endtab %}

{% tab title="DOM Tree" %}
```
Document
└── html
    ├── head
    │   └── title ("My Page")
    └── body
        ├── h1 (id="title") ("Hello, World!")
        ├── p ("This is a paragraph.")
        └── button (id="changeText") ("Click Me")
```
{% endtab %}
{% endtabs %}

### Understanding the DOM tree structure

The DOM tree consists of nodes, which are objects representing parts of the webpage.&#x20;

* The **document** node represents the entire webpage.&#x20;
* **Element** nodes represent HTML elements such as headings, paragraphs, and buttons.&#x20;
* **Attribute** nodes represent attributes such as id, class, and src.&#x20;
* **Text** nodes contain the text inside an element.

For example, in the HTML snippet above, the DOM tree would have an element node representing `<h1>` , an attribute node for the id ("title") attribute, and a text node containing the word “Welcome.” JavaScript can modify any part of this structure dynamically.

### Accessing the DOM in JavaScript

JavaScript interacts with the DOM using the document object, which must first be identified and selected before manipulation.&#x20;

The `getElementById` method allows JavaScript to select elements by their id. The `getElementsByTagName` and `getElementsByClassName` methods allow the selection of multiple elements by tag name or class name. The `querySelector` and `querySelectorAll` methods provide more flexible ways to select elements.

```javascript
// Selecting elements by their id
let titleElement = document.getElementById("title");
console.log(titleElement.textContent);  // Outputs: "Hello, World!"

// Selecting all elements by tag name "p"
let paragraphs = document.getElementsByTagName("p");

// Selecting all elements by class name "btn"
let buttons = document.getElementsByClassName("btn");

// Using query selectors
let firstButton = document.querySelector("button");  // Selects first button
let allButtons = document.querySelectorAll("button");  // Selects all buttons
```

For example, selecting an element with id "title" using document.getElementById("title") retrieves the corresponding `<h1>` element.&#x20;

Selecting multiple paragraphs with `document.getElementsByTagName("p")` returns a collection of all `<p>` elements on the page. Using `querySelector("button")` selects the first button on the page while `querySelectorAll("button")` selects all buttons.

These methods are essential for dynamically modifying web pages, which can then be modified dynamically using JavaScript.

### Key concepts

> * The **Document Object Model (DOM)** is a structured representation of an HTML page that browsers create, allowing JavaScript to interact with and modify web content dynamically.
> * The **browser parses HTML** and constructs the DOM tree, which represents the page as a hierarchy of nodes that JavaScript can access and manipulate.
> * The **DOM tree** consists of different types of **nodes**, including **element nodes** (HTML elements), **attribute nodes** (such as id and class), and **text** nodes (content inside elements).
> * The **document object** in JavaScript represents the entire webpage and provides methods to interact with elements dynamically.
> * JavaScript can **select elements** using methods such as `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, and `querySelectorAll`.
> * The DOM allows dynamic content updates without requiring a full page reload, forming the basis for modern interactive web applications.
> * Understanding the hierarchical structure of the DOM is essential for building and modifying webpages programmatically with JavaScript.
