---
description: >-
  Learn how to create flexible, responsive layouts that adapt to different
  screen sizes and devices and explore best practices in web accessibility.
---

# 522 / Styling webpages with CSS

### TL:DR

CSS (Cascading Style Sheets) is a stylesheet language used to control the visual presentation of web pages by defining styles for elements such as text, colours, layouts, and spacing. It allows developers to separate content from design, ensuring consistency across multiple pages and improving maintainability.&#x20;

CSS can be applied using three main methods: **inline CSS**, which styles individual elements directly within HTML tags; **internal CSS**, which applies styles within a `<style>` block inside the HTML document; and **external CSS**, which is the preferred method for large-scale projects, linking an external `.css` file to multiple web pages for a unified look.

***

### Targets

In this section, you will learn to

* Identify the syntax and structure of CSS, including selectors, properties, and values,
* Apply inline, internal, and external CSS styles to HTML documents,
* Use class and ID selectors to style specific elements,
* Understand the importance of maintaining consistency in design using CSS, and
* Apply basic text formatting, colours, and layout properties using CSS.

***

### Content heading

Text

***

### Key Concepts

> * **CSS (Cascading Style Sheets)** control the visual presentation of HTML elements.
> * There are three ways to **apply CSS**: inline (within elements), internal (inside \<style>), external (linked .css file).
> * **Selectors** target elements using tag names (h1 {}), classes (.class {}), IDs (#id {}), groups (h1, h2, h3 {}), and hierarchy (div p {}).
> * The **box model** defines element structure with content, padding, border, and margin.
> * **Positioning properties** include relative (offset from normal flow), absolute (positioned within nearest ancestor), fixed (relative to viewport), sticky (switches based on scroll).
> * **CSS layouts** are flexbox (single-axis flexible layouts), grid (two-dimensional layouts).
> * **Sizing units** are px (fixed), em/rem (relative to font size), % (relative to parent).
> * **Responsive design** uses media queries to adjust styles based on screen size.
> * **Pseudo-classes** (:hover, :focus) and **pseudo-element**s (::before, ::after) allow dynamic styling and content insertion.
> * **Animations and transitions** enable smooth effects using @keyframes, transition, and animation properties.
> * **Best practice** includes the use of external stylesheets for maintainability, organise CSS with comments, and minimise inline styles for reusable code.



