---
layout: default
title: DOM Manipulation 3
---
# DOM Manipulation 3
If you recall from a previous reading, the DOM (Document Object Model) is "the data representation of the objects that comprise the structure and content of a document on the web."

You can think of the structure of the DOM in terms of *parents* and *children* using a diagram like this:
<div style="display: flex; justify-content: space-evenly; gap: 1ch;">
	<figure style="max-width: 486px">
		<img src="images/pic_htmltree.gif" style="width: 100%">
		<figcaption style="font-style: italic; text-align: center;">from W3 Schools</figcaption>
	</figure>
</div>

Starting from the `<body>` element, there are 2 child element in the `<body>`: an `<a>` and an `<h1>`, each which also have their own attributes and inner text. The corresponding HTML would look something like this:

```html
<body>
  <a href="https://miamioh.edu">My link</a>
  <h1>My header</h1>
</body>
```

Take a look at the following example - how would you describe the structure in terms of *parents* and *children*? You can probably make some guess just by looking at the page, but you'll need to open the inspector or look at the HTML to confirm.

<iframe src="https://replit.com/@sheffie/IMS322-Parent-Child?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>

Each cookie image `<img>` has a `<figcaption>` sibling, both of which are children of a `<figure>` element, which are in turn children of the main `<div>` flex container. Or, looking at it from the other direction, the main `<div>` flex container is the parent element containing 3 `<figure>` children, which in turn each contain one `<img>` child element and one `<figcaption>` child element. 
## Creating and Appending Elements
If you were given a large collection of images in a folder to display in a gallery, you would likely painstakingly manually create flexboxes, `<figure>` elements, and `<img>` elements in your HTML. But what if you were running a baking website that featured a different collection and quantity of cookie recipes each week? Is there a way to automatically generate the HTML if you are given the necessary data?

Let's start with a single photo. If I were to create an object that describes the first cookie photo above, it might look like this:
```js
let cookie1 = {
  imageFile: "images/cookie1.jpg",
  altText: "chocolate chip cookie 1",
  captionText: "Cookie 1"
};
```

I can use JavaScript to create each required element using the `createElement()` method and set the required attributes:

```js
let cookieFigure = document.createElement("figure");
let cookieImage = document.createElement("img");
let cookieCaption = document.createElement("figcaption");

cookieImage.src = cookie1.imageFile; // sets src to "images/cookie1.jpg"
cookieImage.alt = cookie1.altText; // sets alt text to "chocolate chip cookie 1"
cookieCaption.innerText = cookie1.captionText; // sets text to "Cookie 1"
```

Then, I can use the `appendChild()` method to place the child elements in the `<div>` flex container parent (see example below). It may not seem like much now, but with the addition of `for` loops and the right workflow, an approach like this could help automate the process and save a lot of time in the long run.

<iframe src="https://replit.com/@sheffie/IMS322-Creating-and-Appending-Elements?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>