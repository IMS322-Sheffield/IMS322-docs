---
layout: default
title: Style Guide
parent: General
nav_order: 1
---

# Style Guide

This is an IMS322 Coding Style guide.

---
## General

### Lowercase File Names
As in `index.html`, NOT `Index.html` or `INDEX.html`.

### Default Filenames
Use the following default filenames in your projects:
- `index.html`
- `style.css`
- `script.js`

If you need more files (e.g. multiple CSS files), is it OK to use other unique and descriptive names like `footer-style.css`. Indeed, each Replit template in this class will include an `ims322-style.css` file in addition to the standard `style.css` file. You can read more about what the  `ims322-style.css` is for [here](css-framework).

### Image Names
Rename you image files for clarity and simplicity whenever necessary. For example, `dog.jpg` is much easier to type and identify than `neom-9E9NsEiUGxg-unsplash.jpg` or `IMG_1234.JPG`.

### Image Sizes
Ensure that all image files used in your projects are reasonably sized according to their intended use.

We will be using the following screen width targets for all projects (based on [MDN Web Docs recommendations](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries)):
- 480px (mobile)
- 800px (tablet, narrow laptop/desktop windows)
- 1100px (wide laptop/desktop windows)

These sizes are already pre-configured for you in the `ims322-style.css` file media queries.

Modern high-DPI (dots per inch) displays actually scale content. For example, a website with a width of 800px on a 13" MacBook Air actually fills 1600px of the display. It uses 4 pixels (2 in width, 2 in height) to render every 1 pixel of content. 

When considering image sizes, this means that you consider how much of the window width your image files will use, and then double that. For example, an image that will only take up half of the window at the most (e.g. one side of a two-column layout, 550px of window space) does not need to be any wider than 1100px.

When downloading images from [Unsplash](https://unsplash.com), you are usually given the choice of a small, medium, large, or original resolution. Depending on your specific layout, small or medium will likely be the best choice. If you do not 

<div style="display: flex; gap: 1ch;">
	<div><img src="images/building-small.jpg"></div>
	<div><img src="images/building-large.jpg"></div>
</div>



---
## HTML
Compiled from [W3 Schools](https://www.w3schools.com/html/html5_syntax.asp) and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/HTML).


### Use lowercase element names

This:
```html
<div>
  <p>This is a paragraph.</p>
</div>
```
Not this:
```html
<DIV>
  <P>This is a paragraph.</P>
</DIV>
```


### Do not use spaces around equals signs
This:
```html
<img src="headshot.jpg" alt="Headshot">
```
Not this:
```html
<img src = "headshot.jpg" alt = "Headshot">
```


### Use blank lines and indentation to sensibly organize your HTML
These can also be supplemented with comments as needed.

This:
```html
<body>

  <header>
	<h1>My Big Project</h1>
  </header>

  <main>
	<!-- This is an HTML comment. -->
	<p>Tons of great content here.</p>
  </main>

  <footer>
    <p>Did you like my content?</p>
  </footer>

</body>
```

Not this:
```html
<body>
<header>
<h1>My Big Project</h1>
</header>
<main>
<!-- This is an HTML comment. -->
<p>Tons of great content here.</p>
</main>
<footer>
<p>Did you like my content?</p>
</footer>
</body>
```


### Your document should always include one complete html, head, title, and body element
The template in Replit will automatically create these for you, but it can be very easy when copy-pasting to accidentally duplicate or break these elements.
```html
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IMS322 Template</title>
  <link href="ims322-style.css" rel="stylesheet" type="text/css" />
  <link href="style.css" rel="stylesheet" type="text/css" />
  <script src="script.js" defer></script>
</head>

<body>
  <p>Stuff stuff stuff.</p>
</body>

</html>
```


### Naming classes and IDs
Class and ID attributes should be written using the "kebab-case" convention in wh

---
## JavaScript



### Loading JavaScript in HTML
You may see `<script>` tags located within the `<body>` when following tutorials or example online. However, for this class, we will always place our `<script>` tags in the `<head>` with the added `defer` keyword.
```html
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IMS322 Template</title>
  <link href="ims322-style.css" rel="stylesheet" type="text/css" />
  <link href="style.css" rel="stylesheet" type="text/css" />
  <script src="script.js" defer></script>
</head>
```