# Hacksheet 524.1 / Selecting elements in the DOM with JavaScript

### Question 1

What is the Document Object Model (DOM), and how does it align with an HTML page?



***

### Question 2

Explain the difference between the DOM's element, attribute, and text nodes.



***

### Question 3

What does the document object represent in JavaScript?



***

### Question 4

What is the purpose of the method `getElementById` in JavaScript, and how does it work?



***

### Question 5

What is the difference between `querySelector` and `querySelectorAll` ?



***

#### Consider the following HTML structure.

```html
<!DOCTYPE html>
<html>
<head><title>Sample Page</title></head>
<body>
    <h1 id="main-title">Hello, World!</h1>
    <p class="intro">Welcome to the DOM tutorial.</p>
    <p class="intro">JavaScript allows us to modify this dynamically.</p>
    <div id="container">
        <button class="btn">Click Me</button>
        <button class="btn">Press Here</button>
    </div>
</body>
</html>
```

### Question 6

Complete the missing code in these JavaScript snippets.

a. To select the first paragraph element (`<p>`) on the page, use

&#x20;    document.            ("p");

b. To select all buttons inside the `div id="container"`, use

&#x20;   document.querySelectorAll("             .btn");

c. To change the text content of the `<h1>` element, use

&#x20;   document.getElementById("main-title").            = "New Title";



***

### Question 7

What JavaScript syntax should be used to select the heading (`<h1>`) element correctly?



***

### Question 8

What JavaScript syntax should be used to select elements with the class `"intro"` ?



***

### Question 9

What will the following JavaScript code return?

```javascript
document.querySelector("#container .btn").textContent;
```



***

### Question 10

A student states that the DOM is a static representation of the HTML file and does not change once the page is loaded.

Evaluate this claim.

