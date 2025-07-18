# Lab 522 / Styling the museum exhibit web pages with CSS

### Overview <a href="#overview" id="overview"></a>

In this lab, you will **apply CSS styles** to the **museum exhibit webpage** you created in the previous lab. You will improve **typography, layout, colors, and responsiveness** while following best practices in **CSS styling and accessibility**.

### Objectives <a href="#objectives" id="objectives"></a>

* Use **CSS to style a structured webpage**.
* Implement **typography, color schemes, and spacing** for better readability.
* Apply **layout techniques** using **Flexbox and Grid**.
* Ensure **images and navigation menus** are styled and responsive.

### Step 1: Set Up Your CSS File <a href="#step-1-set-up-your-css-file" id="step-1-set-up-your-css-file"></a>

1. Copy and paste the HTMl you prepared from Lab 521 - Structuring web pages with HTML to the same file in Lab 521's directory.
2. Access the file named **`style.css`**.
3.  Link it to your HTML file by adding this line inside the `<head>` section of `ancient_egypt.html`:

    ```html
    <link rel="stylesheet" href="style.css">
    ```

### Step 2: Apply Basic Styling <a href="#step-2-apply-basic-styling" id="step-2-apply-basic-styling"></a>

#### 2.1 Global Styles <a href="#id-21-global-styles" id="id-21-global-styles"></a>

Set a base font, text color, and background color for the entire page:

```css
body {
    font-family: Arial, sans-serif;
    color: #333;
    background-color: #f8f8f8;
    line-height: 1.6;
    margin: 0;
    padding: 0;
}
```

#### 2.2 Header & Navigation <a href="#id-22-header--navigation" id="id-22-header--navigation"></a>

Style the header and navigation menu for a better user experience:

```css
header {
    background-color: #2a2a72;
    color: white;
    text-align: center;
    padding: 20px;
}

nav ul {
    list-style: none;
    padding: 0;
    text-align: center;
}

nav ul li {
    display: inline;
    margin: 0 15px;
}

nav ul li a {
    text-decoration: none;
    color: white;
    font-weight: bold;
}
```

#### 2.3 Main Content Styling <a href="#id-23-main-content-styling" id="id-23-main-content-styling"></a>

```css
section {
    background: white;
    padding: 20px;
    margin: 20px auto;
    width: 80%;
    border-radius: 8px;
    box-shadow: 2px 2px 10px rgba(0, 0, 0, 0.1);
}
```

#### 2.4 Making Images Responsive <a href="#id-24-making-images-responsive" id="id-24-making-images-responsive"></a>

Ensure images scale correctly and maintain aspect ratio:

```css
img {
    width: 100%;
    height: auto;
    border-radius: 5px;
}
```

#### 2.5 Footer Styling <a href="#id-25-footer-styling" id="id-25-footer-styling"></a>

```css
footer {
    background-color: #2a2a72;
    color: white;
    text-align: center;
    padding: 10px;
    margin-top: 20px;
}
```

### Step 3: Extend and Personalise <a href="#step-3-extend-and-personalize" id="step-3-extend-and-personalize"></a>

Use Google Fonts for better typography:

```css
@import url('https://fonts.googleapis.com/css2?family=Open+Sans&display=swap');

body {
    font-family: 'Open Sans', sans-serif;
}
```

Add hover effects to buttons and links:

```css
nav ul li a:hover {
    color: #ffcc00;
}
```

Use CSS Flexbox to center sections:

```css
.container {
    display: flex;
    justify-content: center;
    align-items: center;
}
```

### Step 4: Validate your CSS <a href="#step-4-validate-your-css" id="step-4-validate-your-css"></a>

* Check your styles using Chrome DevTools (Right Click > Inspect).
* Use the W3C CSS Validator to check for errors.

### Self-Assessment Criteria <a href="#self-assessment-criteria" id="self-assessment-criteria"></a>

* Proper use of CSS selectors and styles
* Consistent color scheme and typography
* Navigation menu is readable & styled well
* Images and layout are responsive
* Overall page styling follows best practices

### Extensions <a href="#extensions" id="extensions"></a>

* Add a sidebar and style it.
* Style form elements (if you added a contact form in the previous lab).
* Use CSS Grid for advanced layout structuring.
