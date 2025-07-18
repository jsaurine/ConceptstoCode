# 522 Answer key

#### 1. What is CSS, and what is its primary purpose in web development?

<details>

<summary>View Answer</summary>

CSS (Cascading Style Sheets) is a stylesheet language used to control the presentation and layout of HTML documents. Its primary purpose is to separate content (HTML) from design, allowing developers to define styles, such as colours, fonts, and positioning, ensuring a consistent appearance across web pages.

</details>

#### 2. Describe the three methods of applying CSS to an HTML document.

<details>

<summary>View Answer</summary>

CSS can be applied in three ways:

* **Inline CSS:** Styles are applied directly to an HTML element using the `style` attribute (e.g., `<p style="color: blue;">`).
* **Internal CSS:** Styles are defined within a `<style>` block inside the `<head>` section of an HTML document.
* **External CSS:** A separate `.css` file is linked to the HTML file using the `<link>` tag, enabling consistent styling across multiple pages.

</details>

#### 3. What is the syntax for a CSS rule set?

<details>

<summary>View Answer</summary>

A CSS rule set consists of a **selector** and a **declaration block**, where the declaration block contains **property-value pairs** enclosed in curly braces.

```css

selector {
    property: value;
}
```

Example usage:

```css

p {
    color: blue;
    font-size: 16px;
}
```

</details>

#### 4. Explain the difference between class selectors and ID selectors in CSS.

<details>

<summary>View Answer</summary>

A **class selector** (`.`) is used to style multiple elements that share the same class, whereas an **ID selector** (`#`) applies styles to a single, unique element.

Example:

```css
.class-example {
    color: red;
}
#id-example {
color: blue;
}
```

</details>

#### 5. How can you apply multiple CSS classes to a single HTML element?

<details>

<summary>View Answer</summary>

Multiple classes can be applied to an element by separating class names with spaces.

Example:

```html
<p class="class1 class2">Styled Text</p>
```

The element will inherit styles from both `.class1` and `.class2`.

</details>

#### 6. What is the CSS box model, and what are its components?

<details>

<summary>View Answer</summary>

The CSS box model describes how elements are structured and spaced. It consists of four components:

* **Content:** The actual text or image inside the element.
* **Padding:** The space between the content and border.
* **Border:** A visible or invisible boundary surrounding the element.
* **Margin:** The space outside the border, separating the element from others.

</details>

#### 7. How do padding and margin differ in the CSS box model?

<details>

<summary>View Answer</summary>

**Padding** is the space **inside** an element, between its content and border.

**Margin** is the space **outside** the element, affecting the distance between elements.

</details>

#### 8. Explain the concept of CSS specificity and how it affects the application of styles.

<details>

<summary>View Answer</summary>

CSS specificity determines which styles take precedence when multiple rules apply to the same element. It follows a hierarchy:

* **Inline styles** (`style=""`) have the highest specificity.
* **ID selectors** (`#id`) are more specific than class selectors.
* **Class, attribute, and pseudo-class selectors** (`.class`, `[attribute]`, `:hover`) come next.
* **Element selectors** (`h1`, `p`, `div`) have the lowest specificity.
* If multiple rules have the same specificity, the one that appears **last in the stylesheet** is applied.

</details>

#### 9. What are pseudo-classes in CSS? Provide an example.

<details>

<summary>View Answer</summary>

Pseudo-classes define a special state of an element, such as when a user interacts with it.

Example:

```css
a:hover {
    color: red;
}
```

This changes the text colour of a hyperlink when the user hovers over it.

</details>

#### 10. How can you include comments in a CSS file?

<details>

<summary>View Answer</summary>

Comments in CSS are enclosed within `/* ... */` and are ignored by browsers.

Example:

```

/* This is a comment */
p {
    color: blue;
}
```

</details>

#### 11. Describe the difference between CSS's inline, block, and inline-block display values.

<details>

<summary>View Answer</summary>

**Inline:** Elements appear in the same line as surrounding text, without starting a new line (e.g., `<span>`).

**Block:** Elements take up the full width of their container and start on a new line (e.g., `<div>`).

**Inline-block:** Like inline elements but allows setting width and height.

</details>

#### 12. What is the purpose of media queries in CSS?

<details>

<summary>View Answer</summary>

Media queries allow developers to apply styles based on the device's screen size, resolution, or other characteristics. They are essential for responsive design.

Example:

<pre><code><strong>@media (max-width: 600px) {
</strong>    body {
        background-color: lightgrey;
    }
}
</code></pre>

</details>

