---
description: >-
  HTML provides the fundamental structure of every webpage, defining how content
  is arranged and how elements interact within a document.
---

# 521 Structuring webpages with HTML

### TL:DR

Semantic HTML tags provide meaningful structure to web content, improving accessibility, readability, and SEO. Examples include `<header>`, `<nav>`, `<article>`, and `<footer>`, which clearly define their roles within a webpage. In contrast, non-semantic tags like `<div>` and `<span>` and serve as generic containers without conveying meaning. Using semantic tags enhances user experience by helping browsers, screen readers, and search engines better interpret content. This lesson explores the distinctions between semantic and non-semantic tags, their benefits, and best practices for structuring HTML documents effectively.

***

### Targets&#x20;

In this section, you will learn to

* explain the role of HTML in structuring webpages,
* identify and use key HTML elements (`<head>`, `<body>`, `<header>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`, `<div>`),
* distinguish between the use of semantic and non-semantic HTML tags, their purpose and use,
* structure content using semantic HTML for better accessibility and SEO,
* add hyperlinks, lists, images, and tables to a webpage, and
* use developer tools to inspect and validate HTML code.

***

### HTML fundamentals

HTML provides the fundamental structure of every webpage. It defines how content is arranged and how elements interact within a document. Using semantic HTML improves readability, accessibility, and SEO. This lesson introduces key structural elements and demonstrates how to apply them to create a well-formed webpage. You will also explore how web browsers interpret HTML and how to debug errors using developer tools.

You only need a text editor and a web browser to write HTML. You can use a wide variety of text editors, most of which are free. Check for features such as using colour to highlight code segments and autocomplete features. Some websites allow you to write HTML code and display the results directly in your browser.

HTML documents have the file extension .html, and if saved on your computer, they will usually default to opening up in your web browser. You can view an HTML document as a web page (viewed in the browser) or as the HTML code that generates that page (viewed in a text editor). People new to writing HTML often worry that their code has disappeared even though they can still see the HTML file. It is important to remember that the type of application you use to open the HTML file will impact its display.

### Diving deeper into HTML

HTML tags are the building blocks of webpages and help to structure and sequence the content for the browser to render.

<details>

<summary>HTML tags</summary>

Consider the following snippet of HTML:

```
<p>This is a very small paragraph</p>
```

The `<p>` tag is used to specify a paragraph. Most tags work in pairs and are used to enclose some content. Closing tags always start with a forward slash; in this instance `</p>`.

A paragraph is a fundamental building block of a web page. When your browser displays a web page, there are some rules about how to display it. By default, browsers separate paragraphs with a single blank line, and the text is left justified. You can override the default browser presentation rules by using CSS. The process of processing the HTML for display purposes is called rendering.

You may have encountered the term semantic HTML. This is where tags have been used purposefully to reinforce the meaning of content on a page rather than just define the way it will appear. Semantically correct HTML helps ensure that people and machines can make sense of it. This allows the page to be correctly interpreted by screen readers and other user devices.

</details>

<details>

<summary>HTML page structure</summary>

The entire content for an HTML page is enclosed within a pair of `<html>` tags.

Here is the layout of an elementary HTML page:

```html
<html>
   <head>
      <title>Isaac Computer Science</title>
   </head>

   <body>
      <p>Welcome to Isaac Computer Science</p>
   </body>
</html>
```

The `<head>` section contains any content that doesn't appear directly in the main window of the page. In the example, this section includes the `<title>` that will appear within the tab for the page when it is viewed in a web browser.

![image.png](https://emanuel.instructure.com/courses/11998/files/545294/preview)

Below the head section is the `<body>` which contains the main content of the page. This is the part displayed in your web browser's main rectangular window. The paragraph "Welcome to Isaac Computer Science" is in the body. If you are following HTML tutorials or getting help with your code, someone may ask you to type something in the body, so remember what this means.

Leaving multiple spaces or moving text onto a new line in your code does NOT mean that a space is placed on the page your visitors will see. You have already learned that text marked as a paragraph will be displayed with a blank line before and after the text. If you want an extra blank line anywhere on the page, you can use `<br>`. This tag has no closing tag because it has no content to enclose.

You will notice that some of the lines in the HTML have been indented. This is unnecessary - you could write the markup on a single line if you wish. However, reading and making sense of it would be challenging for a human. Spaces and indentation make your markup more straightforward to follow. You can also use comments in your markup.

```html
<!--This is a comment which will not be displayed--
```

</details>

<details>

<summary>Headings</summary>

Headings are used on web pages to introduce a section of the page. The heading text is larger and sometimes uses a different font. Here is some text that says "Welcome Laura!" on this screenshot of the Isaac Computer Science website.

<img src="https://emanuel.instructure.com/courses/11998/files/545295/preview" alt="image.png" data-size="original">

The HTML code for this text would be:

```
<h1>Welcome Laura!</h1>
```

This example uses a level 1 heading. There are six levels of heading - `<h1>` to `<h6>`. Each number signifies a heading with a decreasing level of priority. The `<h1>` tag is used for the most important heading and, by convention, should be used only once on each page. The other levels can be used as many times as needed. The browser generates text of a decreasing size for each level of heading. However, changing the size and most other aspects of a heading's appearance is possible. You will find out how to do this in the CSS section.

Heading tags also have semantic meaning within the page. You should not tag something as a heading if it isn't one. Search engines use the primary `<h1>` heading tag to summarise and index your page. Other headings can help users trying to skim over the content and provide additional information to users of assistive technology (such as screen readers).

</details>

<details>

<summary>Images</summary>

The image tag `<img>` adds an image to a web page. Imagine you have saved a picture called flower.jpg to the same folder as the HTML file you are using for your web page. Here is how you would display it:

```
<img src="flower.jpg">
```

This tag is a little different from the ones we have studied so far. Firstly, there is no need for a corresponding end tag; just the starting tag on its own is fine. Notice that there is an extra piece of information inside the tag, which is called an attribute.

```
src="flower.jpg"
```

This attribute tells the web page that the source (hence src) of the image is the file flowers.jpg, so the web page will look here for the image.

There are additional attributes you can add to an image tag. All attributes are added inside the tag, which means they are placed before the ending > symbol. You can see examples of this in the code below.

**Alt (alternative text)**

The alt attribute provides some alternative text that describes the image. The attribute helps people using assistive technologies — such as screen readers — understand what the web page image depicts. For example:

```
alt="A pink flower against a green background"
```

Add the alt text attribute inside the `<img>` tag like this:

```
<img src="flower.jpg" alt="A pink flower against a green background">
```

Alt text should provide a good description of the image. Think of it as if you were describing the image to someone unable to see it. Writing "an image" is not as helpful as alt text, and the alt text "a picture of a flower" is slightly more useful but could be improved.

Website providers must ensure the sites are accessible to as many people as possible. It is illegal not to take measures to improve accessibility for sites provided by publicly funded bodies.

**Height and width**

You can use the height and width attributes to change the size of your image in pixels.

```
<img src="flower.jpg" height="300" width="200">
```

Once again, these attributes are placed directly inside the image tag itself. However, it is not recommended that you resize images in this way:

* The original image file must be downloaded to the device before it is resized, which may take a while with a high-resolution image.
* The browser may not be the best tool for resizing the image; a better option is to use a specialist image editing program to get the image looking good at the size needed.
* Care must be taken to keep the aspect ratio the same (as the original image) or the image will look distorted. This can be avoided by using auto as a value for the height or width so that the aspect ratio is maintained.

<img src="https://emanuel.instructure.com/courses/11998/files/545296/preview" alt="image.png" data-size="original">

Our example assumes the image file is in the same folder as the HTML file. This might not always be the case, so here are three examples of how to reference files that are not in the same folder:

| HTML                           | Description                                                             |
| ------------------------------ | ----------------------------------------------------------------------- |
| `<img src="photo.png">`        | photo.png is located in the same folder as the current page             |
| `<img src="images/photo.png">` | photo.png is located in the images folder in the current folder         |
| `<img src=".../photo.png">`    | photo.png os located in the folder one level up from the current folder |

All the examples above are known as relative file paths because they link to an image file by specifying its location relative to the current page. Relative links are useful because they will still work if you need to change your website's domain name or host it on a different web server.

</details>

<details>

<summary>Hyerlinks</summary>

A hyperlink is a piece of text that can be clicked. When clicked, it will transfer you to another page or to a named section on the same page.

Here is an example of how you might create a hyperlink:

{% code overflow="wrap" %}
```html
Click here to <a href="https://www.raspberrypi.org/">visit the Raspberry Pi website</a>
```
{% endcode %}

The tag for a hyperlink is `<a>` . You must also include a href attribute that specifies the link's target. Between the tags is the text that will appear on the page as the active link. By default, all links are underlined and will appear as follows:

* An unvisited link is underlined, and blue
* A visited link is underlined and purple
* An active link is underlined and red

In the figure below, you can see an example of a link that has already been visited.

<img src="https://emanuel.instructure.com/courses/11998/files/545298/preview" alt="image.png" data-size="original">

The `<a>` tag (which stands for anchor) is not the easiest to remember until you use it regularly. The HTML link tag also exists, but it is used for another purpose, which will be discussed in the CSS section.

You can use the `<a>` tag to create hyperlinked images and text. You can also provide links to active phone and email services.

</details>

<details>

<summary>Lists</summary>

A list is a handy thing to have on a web page. You may want to have a list of bullet points, such as the ones on the front page of the Isaac Computer Science website:

<img src="https://emanuel.instructure.com/courses/11998/files/545299/preview" alt="image.png" data-size="original">

A list is created using `<ol>` for an ordered list (each item is numbered) or `<ul>` for an unordered list (each item has a bullet point next to it). Individual items are each added to the list with the `<li>` tag. Here is an example of the markup of an ordered list:

```
   <ol>
       <li>This is the first item</li>
       <li>This is the second item</li>
       <li>This is the third item</li>
   </ol>
```

&#x20;The list will be displayed as shown below. The browser will number each list item (in ascending order) and present it, indented, on a new line.

<img src="https://emanuel.instructure.com/courses/11998/files/545300/preview" alt="image.png" data-size="original">

Lists can also be used to create menus and navigation bars. In this case, the list items will be hyperlinks, and their layout and appearance will be customised using CSS.

</details>

<details>

<summary>Forms</summary>

Forms can be used on a web page to gather data. A form begins and ends with the `<form>` tag. Within the tags, you have a wide choice of controls that can be used.

Here is an example of a simple form that provides a search feature. The form is made up of:

* a text box for the user to type in what they are looking for
* a button to submit the form

<img src="https://emanuel.instructure.com/courses/11998/files/545301/preview" alt="image.png" data-size="original">

The HTML needed to create the form is shown below:

```
   <form>
      <input type="text" name="searchbox" id="searchbox">
      <input type="submit" value="Search">
   </form>
```

&#x20;As you can see, the `<input>` tag has been used to develop both form controls. The `type` attribute determines the type of form control that is created. In the example, `text` is used to create a textbox and `submit` creates a submit button. The submit button is special because it is used to submit the form data (usually to a web server) for processing.

It is vital that the `name` attribute is used for all form controls that collect data because data is submitted to web servers as **name-value pairs**. In this instance, the text box has been given the name `searchbox`. If you typed `elephant` into the search box, the pair  `searchbox="elephant"` would be submitted. Naming input controls can be compared with naming variables in a programming language.

You will observe that the text box also has an `id` attribute. This is often given the same identifier as the `name` attribute but has a different purpose (and can be given a different identifier if you wish). Whilst the `name` attribute is used by a web server to make sense of the data that is submitted from a form, the `id` attribute is used client-side. You will see in the section on JavaScript that you are able to manipulate elements of the page and you will ususually do this by targetting elements by their ids (which must be unique on the page).

If you were to create this form on a HTML page, type something in, and press the button, nothing useful would happen. The page would reload itself and the data you entered would be sent back to the same page via the URL. It is possible to change what happens with the data, but you would need to write a program using a language such as JavaScript to do something more useful. At the moment, the computer has no instructions for what to do with the data on the page you have written, so it does not do anything.

</details>

<details>

<summary>Divisions</summary>

So far, you have seen HTML tags that relate to a specific type of content such as paragraphs or images. The HTML `<div>` tag is used to create page **divisions**. These containers or boxes can contain other elements on the page, such as text, images, or form elements. You can group pieces of content within `<div>` tags and then define a CSS style rule set that will apply to everything in that container. This is particularly useful for page layout as advanced CSS can be used to position these containers (as well as styling their appearance). This way, you can create structural elements such as navigation bars and columns for your page.

Each division must be given a unique ID. In the following example, a division has been created for a page footer and has been given the ID `footer`. This division could always appear below any other content on the page. The style rules could include margins and padding or be used to keep the content in a fixed position on the page.

```html
<div id="footer">
<p>This page is copyright</p>
<p>Last updated: December 2020</p>
</div>
```

</details>

***

### Key Concepts

> * **Semantic HTML tags** clearly describe the purpose of their content, improving readability, accessibility, and SEO.
> * **Examples of semantic tags** include `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, and `<footer>`.
> * **Non-semantic tags** such as `<div>` and `<span>` do not inherently convey meaning but are still useful for styling and layout purposes.
> * **Using semantic tags benefits SEO** by helping search engines understand and rank content more effectively.
> * **Screen readers rely on semantic tags** to provide a better browsing experience for users with visual impairments.
> * **The `<div>` tag is non-semantic**, often used for layout purposes when no suitable semantic tag is available.
> * **The `<section>` tag** is used for grouping related content, while the `<article>` tag is for self-contained, independent content.
> * **The `<nav>` tag** is specifically for navigation menus, making it easier for users and search engines to locate site navigation.
> * **Using `<aside>` appropriately** helps distinguish supplementary content, such as sidebars, from the main content.
> * **Semantic HTML supports collaboration**, making it easier for developers and designers to understand a webpage’s structure.
> * **Browsers apply default styles differently to semantic and non-semantic elements**, reinforcing proper document structure.
> * **Accessibility guidelines emphasise semantic HTML**, as it helps users who rely on assistive technologies navigate the web.
