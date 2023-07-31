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

The stuff here applies to HTML, CSS, and JavaScript.


### Use lowercase file names
`index.html`, NOT `Index.html` or `INDEX.html`.


### Default filenames
Use the following default filenames in your projects:
- `index.html`
- `style.css`
- `script.js`
If you need more files, is it OK to use other descriptive names like `footer-style.css`. For instance, each Replit template in this class will include a second `ims322-style.css` file in addition to the standard `style.css` file.


### Image names
Rename you image files for clarity and simplicity whenever necessary. For example, `scuba.jpg`, NOT `neom-9E9NsEiUGxg-unsplash.jpg` or `IMG_1234.JPG`.


### Image sizes

---
## HTML
Compiled from [W3 Schools](https://www.w3schools.com/html/html5_syntax.asp) and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/HTML).


### Use lowercase element names

This:
```
<div>
  <p>This is a paragraph.</p>
</div>
```
Not this:
```
<DIV>
  <P>This is a paragraph.</P>
</DIV>
```


### Do not use spaces around equals signs
This:
```
<img src="headshot.jpg" alt="My Headshot">
```
Not this:
```
<img src = "headshot.jpg" alt =" My Headshot">
```


### Use blank lines and indentation to sensibly organize your HTML
These can also be supplemented with comments as needed.

This:
```
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
```
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
```
<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"">
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
```
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0"">
  <title>IMS322 Template</title>
  <link href="ims322-style.css" rel="stylesheet" type="text/css" />
  <link href="style.css" rel="stylesheet" type="text/css" />
  <script src="script.js" defer></script>
</head>
```