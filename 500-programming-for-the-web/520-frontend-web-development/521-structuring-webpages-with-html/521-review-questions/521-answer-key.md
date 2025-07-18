---
hidden: true
---

# 521 / Answer key

### Question 1

The primary purpose of **HTML** in web development is

* [ ] A. defining styling rules for webpage elements.
* [ ] B. creating interactive features using scripting.
* [x] C. structuring and organising the content of a webpage.
* [ ] D. connecting webpages to databases

### **Question 2**

Which of the following HTML elements is **semantic** and provides meaning about the content inside it?

* [ ] A. \<div>
* [ ] B. \<span>
* [x] C. \<section>
* [ ] D. \<br>

### Question 3

Which tag should be used to insert a **hyperlink** in HTML?

* [ ] A. `<h>`
* [x] B. `<a>`
* [ ] C. `<src>`
* [ ] D. `<url>`

### Question 4

The **alt** attribute in the `<img>` tag

* [ ] A. links the image to another page.
* [x] B. adds a caption to the image.
* [ ] C. provides alternative text when the image cannot load.
* [ ] D. applies inline styling to the image.&#x20;

### Question 5

Which tags should be nested to create a navigation menu?

* [ ] A. `<menu>`  / `<li>` / `<ul>`&#x20;
* [ ] B. `<menu>`  / `<ul>` / `<li>`&#x20;
* [ ] C. `<nav>`  / `<li>` / `<ul>`&#x20;
* [x] D. `<nav>`  / `<ul>` / `<li>`&#x20;

***

### Question 6 (3 marks)

Compare the use of semantic and non-semantic HTML tags and give an example of each.

<details>

<summary>See answer</summary>

**Semantic HTML tags** clearly describe the meaning and purpose of their content, improving accessibility and readability. An example is `<article>`, which represents a self-contained piece of content like a blog post.\
**Non-semantic HTML tags**, like `<div>`, do not provide any meaning about their content’s role—they are generic containers used mainly for layout and grouping elements.\
Using semantic tags helps screen readers and search engines better understand the structure and context of the webpage.

</details>

### Question 7 (3 marks)

Identify and describe how attributes are used in the tag used to place images.

<details>

<summary>See answer</summary>

The tag used to place images in HTML is the `<img>` tag. It uses several important **attributes** to define how the image behaves:

* The `src` attribute specifies the **file path or URL** of the image to be displayed (e.g., `src="photo.jpg"`).
* The `alt` attribute provides **alternative text** that describes the image, which improves accessibility and appears if the image fails to load.
* Additional attributes like `width`, `height`, and `title` can control the size of the image and provide extra information as a tooltip.

These attributes ensure the image is displayed correctly and the content remains accessible to all users.

</details>

### Question 9 (4 marks)

Suggest improvements to the following HTML code to improve accessibility. Refer to line numbers in your response.

{% code lineNumbers="true" %}
```html
<html>
<head><title>About Me</title></head>
<body>
  <div>
    <h1>My Website</h1>
    <p>Click here to see my portfolio</p>
    <img src="me.jpg">
  </div>
</body>
</html>
```
{% endcode %}

<details>

<summary>See answer</summary>

* **Line 1**: Added `lang="en"` to `<html>` for screen reader language identification.
* **Line 4–10**: Used semantic elements like `<main>` and `<header>` for structure.
* **Line 8**: Wrapped link text in an `<a>` tag for proper keyboard navigation and screen reader access.
* **Line 9**: Added `alt` text to the image to describe it for visually impaired users.

</details>
