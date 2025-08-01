---
description: Learn how HTML provides the structural foundation for all webpages.
---

# 521 Structuring webpages with HTML

### Overview

In this topic, we explore how HTML is used to structure the content of webpages. Students learn how to define headings, paragraphs, links, images, and semantic layout elements using HTML tags. These tags create the building blocks of websites, providing structure and meaning for both browsers and users. A strong understanding of HTML is essential before applying styling with CSS or adding interactivity with JavaScript.

### Targets

In this topic, students learn to:

* Define and use common HTML tags
* Structure content using semantic HTML elements
* Create hyperlinks, headings, lists, and media
* Apply proper nesting and indentation
* Validate HTML to ensure correct syntax and accessibility

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Designing web applications**

* Model elements that form a web development system\
  – client-side (front-end) web programming

</details>

### What is HTML?

**HTML (HyperText Markup Language)** is the standard language used to define the structure of webpages. It tells the browser what each part of the content means—for example, which text is a heading, which part is a list, or where an image should appear.

#### Common HTML tags

* `<h1>` to `<h6>` – Headings
* `<p>` – Paragraph
* `<a>` – Link (anchor)
* `<img>` – Image
* `<ul>`, `<ol>`, `<li>` – Lists
* `<div>`, `<span>` – Generic containers
* `<section>`, `<article>`, `<footer>` – Semantic layout

Tags are nested inside each other to show structure, and elements are enclosed in opening and closing tags: `<tag> ... </tag>`

### Page structure example

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My First Webpage</title>
  </head>
  <body>
    <h1>Welcome</h1>
    <p>This is my first webpage built with HTML.</p>
    <a href="https://example.com">Visit example</a>
  </body>
</html>
```

### Semantic HTML

**Semantic HTML** uses tags that describe the purpose of the content, not just how it looks. This improves accessibility, SEO, and maintainability.

Examples:

* `<header>` – top section of a page
* `<nav>` – navigation menu
* `<main>` – main content
* `<article>` – self-contained content
* `<footer>` – bottom section of the page

### Good practices

* Use consistent **indentation** to reflect tag hierarchy
* Close all tags properly
* Validate code using an HTML validator (e.g. [W3C validator](https://validator.w3.org/))
* Avoid using HTML for styling—leave that to CSS

### Summary

HTML defines the structure of a webpage using nested tags. It gives meaning to content, enabling browsers to display it correctly and assistive technologies to interpret it accurately. Mastering HTML is the first step toward building dynamic, styled, and accessible web applications.
