---
description: >-
  Apply semantic HTML tags to create the structure and sequence of HTML tags on
  a web page.
---

# Lab 521 / Structuring webpages with semantic HTML

### Overview <a href="#overview" id="overview"></a>

In this lab, you will take **unstructured text** about a museum exhibit and convert it into a **well-structured HTML document** using semantic elements. This activity will help you understand the **importance of proper HTML structure, accessibility, and SEO best practices**.

### Objectives <a href="#objectives" id="objectives"></a>

* Use **semantic HTML tags** to structure content correctly.
* Implement a **logical document structure** with headings, sections, and navigation.
* Ensure **accessibility** and **readability**.
* Include images and colours as appropriate.
* Avoid overuse of `<div>` by using meaningful HTML elements.

### Scenario: Museum Exhibit Webpage <a href="#scenario-museum-exhibit-webpage" id="scenario-museum-exhibit-webpage"></a>

The **National History Museum** is launching a new exhibit, _The Wonders of Ancient Egypt_. Your task is to convert **plain text content** into a **properly structured HTML document** for their website.

### Given Copy (Raw Text) <a href="#given-copy-raw-text" id="given-copy-raw-text"></a>

\`The following text will be transformed into a structured HTML document:

{% code overflow="wrap" %}
```
The Wonders of Ancient Egypt

Welcome to our latest exhibit:
The Wonders of Ancient Egypt

This exhibit explores the art, architecture, and daily life of one of the world’s most fascinating civilizations.

Key Highlights:
• The Great Pyramids and their construction
• The discovery of King Tutankhamun’s tomb
• Daily life in ancient Egyptian society

Exhibit Details:
The exhibit is open from March 1, 2025, to August 31, 2025.

Location:
National History Museum, Main Hall

Tickets: 
$10 for students, free for children under 12

Explore More:
Visit our gift shop for exclusive Ancient Egypt-themed items.
Attend our guest lecture series featuring Egyptologists from around the world.

Contact Us:
Email: info@nationalhistorymuseum.com
Phone: (123) 456-7890
```
{% endcode %}

### Instructions <a href="#instructions" id="instructions"></a>

1. **Access the file** named `ancient_egypt.html`.
2. **Structure the content using semantic HTML**, ensuring:
   * A `<header>` for the exhibit title and introduction.
   * A `<nav>` for links to different sections.
   * A `<main>` containing `<section>` elements for structured content.
   * A `<footer>` for contact details.
3. **Ensure accessibility** by:
   * Using `<strong>` for important information.
   * Providing meaningful `<a>` text for links.
   * Placing all list items inside `<ul>` or `<ol>`.
4. **Validate your HTML** using [W3C Validator](https://validator.w3.org/).

### Self-Assessment Criteria <a href="#self-assessment-criteria" id="self-assessment-criteria"></a>

* Proper use of semantic HTML (no `<div>` misuse)
* Logical structure using headings and sections
* Lists, links, and navigation are formatted correctly
* Contact information is placed in a proper footer
* Accessibility best practices followed

### Example HTML Structure <a href="#example-html-structure" id="example-html-structure"></a>

Your final HTML should resemble the following **(but modified with your own styling and enhancements)**:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Wonders of Ancient Egypt</title>
</head>
<body>

    <header>
        <h1>The Wonders of Ancient Egypt</h1>
        <p>Explore the art, architecture, and daily life of one of the world's most fascinating civilizations.</p>
    </header>

    <nav>
        <ul>
            <li><a href="#highlights">Key Highlights</a></li>
            <li><a href="#details">Exhibit Details</a></li>
            <li><a href="#extras">Explore More</a></li>
            <li><a href="#contact">Contact Us</a></li>
        </ul>
    </nav>

    <main>
        <section id="highlights">
            <h2>Key Highlights</h2>
            <ul>
                <li>The Great Pyramids and their construction</li>
                <li>The discovery of King Tutankhamun's tomb</li>
                <li>Daily life in ancient Egyptian society</li>
            </ul>
        </section>

        <section id="details">
            <h2>Exhibit Details</h2>
            <p><strong>Dates:</strong> March 1, 2025 – August 31, 2025</p>
            <p><strong>Location:</strong> National History Museum, Main Hall</p>
            <p><strong>Tickets:</strong> $15 for adults, $10 for students, free for children under 12</p>
        </section>

        <section id="extras">
            <h2>Explore More</h2>
            <p>Visit our <strong>gift shop</strong> for exclusive Ancient Egypt-themed items.</p>
            <p>Attend our <strong>guest lecture series</strong> featuring Egyptologists from around the world.</p>
        </section>
    </main>

    <footer id="contact">
        <h2>Contact Us</h2>
        <p><strong>Email:</strong> <a href="mailto:info@nationalhistorymuseum.com">info@nationalhistorymuseum.com</a></p>
        <p><strong>Phone:</strong> (123) 456-7890</p>
    </footer>

</body>
</html>
```
