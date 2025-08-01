---
description: >-
  Learn how to create flexible, responsive layouts that adapt to different
  screen sizes and devices and explore best practices in web accessibility.
---

# 522 Styling webpages with CSS

### 522 Styling webpages with CSS

Learn how CSS controls the appearance and layout of web content.

### Overview

In this topic, we explore how CSS (Cascading Style Sheets) is used to style HTML content. Students learn how to define colours, fonts, layouts, and spacing using rules that apply to specific elements or groups of elements. By separating structure (HTML) from presentation (CSS), developers can keep their code modular, reusable, and easier to maintain.

### Targets

In this topic, students learn to:

* Define CSS rules and apply them to HTML elements
* Use classes, IDs, and selectors to target elements
* Modify text, colour, spacing, borders, and backgrounds
* Apply box model concepts to control layout
* Organise styles using external and internal stylesheets
* Understand how cascading and specificity affect styling

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Designing web applications**

* Investigate cascading style sheets (CSS) and its impact on the design of a web application\
  – consistency of appearance\
  – flexibility with browsers or display devices\
  – CSS maintenance tools

</details>

### What is CSS?

**CSS (Cascading Style Sheets)** is a language used to style and visually format HTML content. It allows developers to define how elements look on the page—including colour, size, layout, and spacing.

CSS keeps styling separate from content, which improves reusability, accessibility, and responsive design.

### CSS syntax and selectors

A CSS rule consists of a **selector** and a **declaration block**:

```css
p {
  color: navy;
  font-size: 16px;
}
```

* The selector `p` targets all paragraph elements
* The declarations inside the braces define the appearance

#### Types of selectors

* `element` – targets all elements of a type (`h1`, `p`)
* `.class` – targets elements with a specific class
* `#id` – targets a unique element with a specific ID

### Applying CSS to HTML

There are three ways to add CSS:

1. **External stylesheet** – linked using `<link>` in `<head>`
2. **Internal stylesheet** – placed in a `<style>` tag in the HTML document
3. **Inline style** – added directly in an element’s `style` attribute (not recommended)

### The box model

Every HTML element is treated as a rectangular box with four layers:

* **Content** – text or image
* **Padding** – space between content and border
* **Border** – surrounds the padding
* **Margin** – space outside the border

Understanding the box model is essential for layout and spacing.

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Cascading and specificity

When multiple rules target the same element, CSS uses **cascading order** and **specificity** to determine which rule applies. For example:

* Inline styles > ID selectors > class selectors > element selectors
* Later rules override earlier ones if specificity is equal

### Summary

CSS gives webpages their appearance by applying visual styles to structured content. It separates design from layout, enabling developers to create consistent, responsive, and professional-looking websites. Mastery of CSS is essential for front-end development.
