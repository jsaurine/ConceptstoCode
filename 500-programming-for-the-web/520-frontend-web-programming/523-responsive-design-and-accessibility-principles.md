---
description: >-
  Learn how to design webpages that adapt to different devices and support
  inclusive, accessible experiences for all users.
---

# 523 Responsive design and accessibility principles

### Overview

In this topic, we explore how responsive design and accessibility work together to ensure that web content is usable on any device and by all users. Students learn how to use flexible layouts, relative sizing, and media queries to build mobile-friendly designs, while also applying accessibility guidelines to support users with diverse needs. These principles are essential for creating ethical, inclusive and effective web applications.

### Targets

In this topic, students learn to:

* Define responsive design and describe its importance
* Use media queries and flexible layouts to support multiple screen sizes
* Apply semantic HTML and ARIA roles to improve accessibility
* Follow best practices for colour contrast, keyboard navigation, and alternative text
* Evaluate webpages for inclusivity using browser accessibility tools

### Syllabus references

<details>

<summary><a href="https://curriculum.nsw.edu.au/learning-areas/tas/software-engineering-11-12-2022/content/year-12/fa6aab137e"><strong>Programming for the web</strong></a></summary>

**Designing web applications**

* Investigate cascading style sheets (CSS) and its impact on the design of a web application\
  – consistency of appearance\
  – flexibility with browsers or display devices
* Investigate and explain the role of the World Wide Web Consortium (W3C) in the development of applications for the web\
  – Web Accessibility Initiative (WAI)\
  – accessibility

</details>

### What is responsive design?

**Responsive design** means building webpages that automatically adapt to different screen sizes and devices. A responsive site might rearrange content, scale images, or change font sizes when viewed on a mobile phone versus a desktop monitor.

Techniques include:

* **Relative units** (e.g. `em`, `%`, `vw`) instead of fixed pixels
* **Fluid grids** that adjust column sizes
* **Media queries** to apply styles conditionally based on screen size

```css
@media screen and (max-width: 600px) {
  .nav-menu {
    display: none;
  }
}
```

This CSS hides a navigation menu on screens narrower than 600 pixels.

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption><p>Responsive design ensures that webpages adjust automatically to fit different screen sizes, improving usability and accessibility across devices.</p></figcaption></figure>

### Accessibility principles

**Accessibility** means designing webpages so people with disabilities or impairments, such as vision loss, motor difficulties, or dyslexia, can use them.

Core principles include:

* **Text alternatives** – for images (`alt` attributes) and icons
* **Keyboard accessibility** – ensure all functionality is reachable without a mouse
* **Semantic HTML** – use tags that describe content (e.g. `<nav>`, `<main>`, `<button>`)
* **Colour contrast** – provide sufficient contrast between text and background
* **Captions and transcripts** – for audio or video content

The **Web Accessibility Initiative (WAI)** from the W3C provides internationally recognised guidelines, including the **WCAG (Web Content Accessibility Guidelines)**.

### Tools for testing accessibility

Modern browsers include built-in accessibility evaluation tools. These can be used to:

* Highlight missing alt attributes or ARIA roles
* Test keyboard navigation and tab order
* Simulate vision impairments (e.g. colour blindness, screen readers)

Online tools like [WAVE](https://wave.webaim.org/) and browser extensions like Axe DevTools also support accessibility audits.

### Summary

Responsive design and accessibility ensure that web applications are usable across devices and inclusive of all users. By combining flexible layouts with semantic structure and thoughtful interface choices, developers can create web content that is ethical, user-friendly, and aligned with best practice standards.
