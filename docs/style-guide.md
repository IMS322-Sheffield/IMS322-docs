---
layout: default
title: Style Guide
nav_order: 1
---
# IMS322 Style Guide
Many companies, large and small (e.g. Google, Airbnb, and more), adopt style guides to ensure that everyone writes similar well-organized code. Sloppy or inconsistent code might still technically work, but it can be difficult to read, share, or debug.

The **IMS322 Style Guide** has been assembled from excerpts from reputable sources. You should reference this guide regularly whenever working on class exercises or assignments until it becomes second nature. Although it includes many widely adopted conventions, it is by no means intended to be the "best" or "correct" approach — after taking this class, you might consider other coding styles based on personal or professional preference.

Some of the points awarded on each coding assignment will be based on how well you adhere to this guide. However, many of the style conventions below can be applied automatically if you use the formatting tools in CodePen and Codespaces (notable exceptions being image file, class, id, variable, and function naming and image file organization).

---
## General

### Default filenames
- `index.html`
- `style.css`
- `script.js`

### Simplify image names and organization
Rename long or cryptic image files whenever necessary. For example, `dog.webp` is much easier to type and identify than `neom-9E9NsEiUGxg-unsplash.webp`.

When working with multiple image files, put them all in an "images" folder to help keep the file browser organized. Keep in mind, this means that the `src` attribute of your `<img>` elements will needs to include the folder as part of the file name e.g. `images/dog.webp`.
### Media queries and display size targets
Your project layouts will need to work well at the following window widths (based on [MDN Web Docs recommendations](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS#mobile-first_media_queries)):
- 480px (mobile)
- 800px (tablet, narrow laptop/desktop windows)
- 1100px (wide laptop/desktop windows)

Media queries for `480px` and `800px` widths will be pre-configured for you in every project's `style.css` file to use as needed.

---
## HTML
Excerpted from [W3 Schools](https://www.w3schools.com/html/html5_syntax.asp) and [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/HTML).
### Do not use spaces around equals signs for attributes
```html
<img src="headshot.webp" alt="Headshot">
```
### Naming classes and IDs
Class and ID attributes should always be written using the the "kebab-case" convention in which lowercase words are separated by hyphens. Write concise, searchable, and meaningful names. Only use common and easy-to remember abbreviations when a name becomes excessively long.
```html
<p class="kebab-case" id="kebab-case">
  Blah blah blah.
</p>
```
### Organize HTML with blank lines, indentation, and comments
#### This:
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
    <p>Like and subscribe!</p>
  </footer>

</body>
```
#### Not this:
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
<p>Like and subscribe!</p>
</footer>
</body>
```

---
## CSS
Portions excerpted from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/CSS).
### Use relative units by default
Recommended relative units:
- `%` - Percentage relative to the parent element. 
- `ch` - The width of the number "0" of the element's font.
- `rem`	- Relative to the default browser font size.
- `vw` - 1% of the viewport's (window) width.
- `vh` - 1% of the viewport's (window) height.

In some cases, you may still find that the absolute unit `px` is the best fit. Some examples:
- If you want to ensure that a small image in a flexible container never stretches beyond its original resolution, set a `max-width` property in `px`.
- If you want to have specific control over the roundness of box corners, set `border-radius` in `px`.

You can read more about all the valid absolute and relative units in this [MDN Web Docs reference](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#numbers_lengths_and_percentages).
### Use HEX or RGB color syntax
This will help ensure consistency with your wireframe application colors.
- Example HEX code: `#E9967A`
- Example RGB code: `rgb(233, 150, 122)`

There are multiple color helpers on the [Utilities](utilities.md) page.
### Do not style with ID selectors
Use element and class selectors.
#### This:
```css
h2 {
  color: blue;
}

.important-text {
  color: red;
  font-weight: bold;
}
```
#### Not this:
```css
#important-text {
  color: red;
  font-weight: bold;
}
```
### Organize CSS with blank lines, indentation, and comments
#### This:
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
#### Not this:
```css
h2 {
font-size: 2.4rem;
}
h3 {
text-shadow: 1px 1px 2px red;
font-size: 2rem;
}
```

---
## JavaScript
Excerpted from [MDN Web Docs](https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Writing_style_guide/Code_style_guide/JavaScript) and [JavaScript Standard Style](https://standardjs.com/rules.html).
### Loading JavaScript in HTML
Always put your `<script>` tags in the `<head>` element with the added `defer` keyword (not required when working in CodePen).
```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link rel="stylesheet" href="style.css" />
  <script src="script.js" defer></script>
  <title>IMS322</title>
</head>
```
### Declare variables with `let` and `const`, not `var`
Use the keywords `let` (for values that will change) and `const` (for values that will not change) when declaring variables. Although it is still technically valid, do not use the outdated `var`.
```js
let favoriteFruit = "apple";
const birthYear = 1986;
```
### Use semicolons at the end of every statement
```js
let favoriteFruit = "apple";
```
### Use double quotes for strings
```js
console.log("hello");
```
### Add a space around operators and equals signs
```js
const exampleOperation = exampleNumber * 2;
```
### Do not use extra spaces inside parentheses
```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}
```
### Always use `===` instead of `==` in `if` statements
```js
if (name === "John") {
  // stuff
}
```
### Naming variables and functions
Variables and functions should be written using the "camelCase" convention in which each word (except the first) starts with a capital letter (without spaces or hyphens). Write concise, searchable, and meaningful names. Only use common and easy-to remember abbreviations if a name becomes excessively long.
```js
const favoriteFruit = "apple";
```
### Curly brace spacing
When using curly braces (e.g. in `if` statements and `function` declarations), the opening brace should be on the same line as the corresponding keyword. There should also be a space before the opening bracket.
```js
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}

function declareLove() {
  console.log("I love everything!");
}
```
### Organize JavaScript with blank lines, indentation, and comments
#### This:
```js
// This is a JavaScript comment
if (favoriteFruit === "apple") {
  console.log("I like apples, too!");
}

function declareLove() {
  console.log("I love everything!");
}
```
#### Not this:
```js
if (favoriteFruit === "apple") {
console.log("I like apples, too!");
}
function declareLove() {
console.log("I love everything!");
}
```