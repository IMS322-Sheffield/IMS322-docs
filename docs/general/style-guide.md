---
layout: default
title: Style Guide
parent: General
nav_order: 1
---

# IMS322 Style Guide

A Coding Style Guide contains a set of rules and guidelines for writing code. While some code errors are absolute (e.g. misspelling the name of a variable or function), some other things like blank space and capitalization can be more forgiving.

---
## General

### Lowercase file names
As in `index.html`, NOT `Index.html` or `INDEX.html`.

### Default filenames
Use the following default filenames in your projects:
- `index.html`
- `style.css`
- `script.js`

If you need more files (e.g. multiple CSS files), is it OK to use other unique and descriptive names like `footer-style.css`. Indeed, each Replit template in this class will include an `ims322-style.css` file in addition to the standard `style.css` file. You can read more about what the  `ims322-style.css` is for [here](css-framework).

### Image names
Rename you image files for clarity and simplicity whenever necessary. For example, `dog.jpg` is much easier to type and identify than `neom-9E9NsEiUGxg-unsplash.jpg` or `IMG_1234.JPG`.

### Image sizes
Ensure that all image files used in your projects are reasonably sized according to their intended use.

We will be using the following screen width targets for all projects (based on [MDN Web Docs recommendations](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries)):
- 480px (mobile)
- 800px (tablet, narrow laptop/desktop windows)
- 1100px (wide laptop/desktop windows)

These sizes are already pre-configured for you in the `ims322-style.css` file media queries.

Modern high-DPI (dots per inch) displays actually scale content. For example, a website with a width of 800px on a 13" MacBook Air actually fills 1600px of the display. It uses 4 pixels (2 in width, 2 in height) to render every 1 pixel of content. 

When considering image sizes, this means that you consider how much of the window width your image files will use, and then double that. For example, an image that will only take up half of the window at the most (e.g. one side of a two-column layout, 550px of window space) does not need to be any wider than 1100px.

When downloading images from [Unsplash](https://unsplash.com), you are usually given the choice of a small, medium, large, or original resolution. Depending on your specific layout, small or medium will likely be the best choice. If you do not 

The two images below are each inside of `<div>` elements that have the property `max-width: 320px`. Even though they look identical, the one on the left was the "small" size option on Unsplash, while the one on the right was the "large" option. The small version is only 640X490 pixels and 223KB, while the large one is 2400X3600 and 2MB!

<div style="display: flex; justify-content: space-evenly; gap: 1ch;">
	<figure style="max-width: 320px">
		<img src="images/building-small.jpg" style="width: 100%">
		<figcaption style="font-style: italic;">640X490 original resolution</figcaption>
	</figure>
	<figure style="max-width: 320px">
		<img src="images/building-large.jpg" style="width: 100%">
		<figcaption style="font-style: italic;">2400X3600 original resolution</figcaption>
	</figure>
</div>

---
## HTML
Excerpted from [W3 Schools](https://www.w3schools.com/html/html5_syntax.asp) and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/HTML).

### Lowercase element names

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


### Use blank lines, indentation, and comments to sensibly organize your HTML
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
Class and ID attributes should be written using the "kebab-case" convention in which multiple all-lowercase words are separated by hyphens.
```html
<p class="kebab-case-class" id="kebab-case-id">Blah blah blah.</p>
```

Use concise, searchable, and meaningful names. Only use common and easy to remember abbreviations when a name becomes excessively long. A class name called `main-red-text` is much easier to find and recall than `mn-rd-txt`. Similarly, the ID `answer1-button` is much easier to find and recall than `button1`.

### Semantic HTML
A [semantic HTML](https://developer.mozilla.org/en-US/docs/Glossary/Semantics#semantics_in_html) element describes its meaning, providing context for the developer, browser, and user. It also improves accessibility for people that use screen readers. Some examples of common semantic HTML elements are:
- `<h1>`, `<h2>`, `<h3>`, etc.
- `<header>`
- `<main>`
- `<nav>`
- `<section>`

Try to use the most appropriate [HTML tags](https://developer.mozilla.org/en-US/docs/Web/HTML/Element) whenever possible. When your content does not clearly fit into a semantic element, non-semantic elements like `<div>` are fine.

---
## CSS
Portions excerpted from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries).

### Plan your CSS
Before diving in and writing huge chunks of CSS, plan your styles carefully. What general styles are going to be needed, what different layouts do you need to create, what specific overrides need to be created, and are they reusable? Above all, you need to try to avoid too much overriding. If you keep finding yourself writing styles and then cancelling them again a few rules down, you probably need to rethink your strategy. *This is especially important for responsive layouts like Flexbox.*

### Use flexible/relative units
For maximum flexibility over the widest possible range of devices, it is a good idea to size containers, padding, etc. using relative units like `ems` and `rems` or percentages and viewport units if you want them to vary depending on viewport width. You can read some more about this in the MDN Web Docs guide to [CSS values and units](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries).

The only absolute unit recommended is `px`, and only when it is the best fit. Some examples:
- If you want to ensure that an image never displays larger than its original resolution, you can set the `max-width` in `px`.
- If you want to have specific control over the roundness of box corners, you can set the `border-radius` in `px`.

Recommended relative units:
- `%` - Percentage relative to the parent element. 
- `ch` - The width of the number "0" of the element's font.
- `rem`	- Relative to the default browser font size.
- `vw` - 1% of the viewport's width.
- `vh` - 1% of the viewport's height.

### Use blank lines, indentation, and comments to sensibly organize your CSS
```css
/* This is a CSS comment */
h2 {
  font-size: 2.4rem;
}

h3 {
  /* Creates a red drop shadow */
  text-shadow: 1px 1px 2px red;
  font-size: 2rem;
}
```

### Apply CSS using classes
Unless you are applying a style property broadly (e.g. you want *all* `h2` elements to be blue), use class selectors whenever possible.

In HTML:
```html
<h2>This is a level 2 heading.</h2>
<p class="warning-text">This is warning text for really important stuff.</p>

```

In CSS:
```css
/* An element selector */
h2 {
  color: blue;
}

/* A class selector */
.warning-text {
  color: red;
  font-weight: bold;
}
```

---
## JavaScript
Excerpted from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/JavaScript) and [JavaScript Standard Style](https://standardjs.com/rules.html).

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

### Declare variables with `let` and `const`
Use the keywords `let` (for values that will change) and `const` (for values that will not change) when declaring variables. Although it will still work, do not use the outdated `var`.

### Use single quotes for strings
```js
console.log('hello');
```

### Add a space after keywords and around operators and equals signs
This:
```js
const exampleNumber = 10;
const exampleOperation = exampleNumber * 2;

let favoriteFruit = 'apple';

if (favoriteFruit === 'apple') {
  console.log('I like apples, too!');
}
```

Not this:
```js
const exampleNumber=10;
const exampleOperation=exampleNumber*2;

let favoriteFruit='apple';

if(favoriteFruit==='apple') {
  console.log('I like apples, too!');
}
```

### Do not use spaces inside parentheses
This:
```js
if (favoriteFruit === 'apple') {
  console.log('I like apples, too!');
}
```
Not this:
```js
if ( favoriteFruit === 'apple' ) {
  console.log( 'I like apples, too!' );
}
```

### Always use `===` instead of `==` in `if` statements
This:
```js
if (name === 'John')
```
Not this:
```js
if (name == 'John')
```

### Naming variables and functions
Variables and functions should be written using the "camelCase" convention in which each word after the first one starts with a capital letter (without spaces or hyphens). 
```js
const favoriteFruit = 'apple';
```

Use concise, searchable, and meaningful names. Only use common and easy to remember abbreviations when a name becomes excessively long.

## Curly brace spacing
When using curly braces (e.g. in `if` statements, `for` loops, and `function` declarations), the opening brace should be on the same line as the corresponding keyword. There should also be a space before the opening bracket.
```js
if (favoriteFruit === 'apple') {
  console.log('I like apples, too!');
}

for (const car of allCars) {
  car.paint("red");
}

function declareLove() {
  console.log('I love everything!');
}
```

### Use blank lines, indentation, and comments to sensibly organize your JavaScript
This:
```js
// This is a JavaScript comment
if (favoriteFruit === 'apple') {
  console.log('I like apples, too!');
}

for (const car of allCars) {
  car.paint("red");
}

function declareLove() {
  console.log('I love everything!');
}
```

Not this:
```js
if (favoriteFruit === 'apple') {
console.log('I like apples, too!');
}
for (const car of allCars) {
car.paint("red");
}
function declareLove() {
console.log('I love everything!');
}
```