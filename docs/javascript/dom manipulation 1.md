---
layout: default
parent: JavaScript
title: DOM Manipulation 1
nav_order: 9
---
# DOM Manipulation
The Document Object Model, or *DOM*, is "the data representation of the objects that comprise the structure and content of a document on the web."

So far, we have primarily used JavaScript to add or remove classes on HTML elements or generate messages in the console. To take the next step with JavaScript, we want to start directly manipulating the HTML itself. However, JavaScript cannot understand HTML the way that it is written.

Clearly, 
```html
<h1>Hello</h1>
```
looks very different than
```js
let myVariable = 'banana'
```

Think of the DOM as a translation of HTML that JavaScript can understand. It defines:
- The HTML elements as **objects** (the way an HTML element is treated when assigned to a variable)
- The **properties** of all HTML elements (`classList`, which we used for toggling classes, is an example of a property)
- The **methods** to access all HTML elements (`toggle()`, which we used with `classList`, is an example of a method)
- The **events** for all HTML elements (for example, the `'click'` event that fires when a button is clicked)

Technically, we have already started working with the DOM by using event listeners and toggling classes. Now, we will go a couple steps further.

## Manipulating Text
To change the text displayed in an HTML element from JavaScript, use the `innerText` method:

```js
element.innerText = 'hello'
```

<iframe src="https://replit.com/@sheffie/IMS322-DOM-innerText?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
## Manipulating Values
Some HTML elements, notably `<button>` and `<input>`, can have a value attribute. This attribute is a way to read, store, or change some information - usually, a number - that is associated specifically with that element.

Take a look at the 3 sliders - `<input>` elements with `type="range"` - in the example below. Each one is written with a different initial value attribute, which is why they all start at different positions (sliders have a range from 0 to 100 by default).

<iframe src="https://replit.com/@sheffie/IMS322-Values?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>

These values can be read in JavaScript (e.g. in response to changes to the slider made by the user), but they can also be set from JavaScript.

<iframe src="https://replit.com/@sheffie/IMS322-DOM-Values?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>