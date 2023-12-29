---
layout: default
title: DOM Manipulation 1
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
let myVariable = "banana";
```

Think of the DOM as a translation of HTML that JavaScript can understand. It defines:
- The HTML elements as **objects** (the way an HTML element is treated when assigned to a variable)
- The **properties** of all HTML elements (`classList`, which we used for toggling classes, is an example of a property)
- The **methods** to access all HTML elements (`toggle()`, which we used with `classList`, is an example of a method)
- The **events** for all HTML elements (for example, the `"click"` event that fires when a button is clicked)

Technically, we have already started working with the DOM by using event listeners and toggling classes. Now, we will go a couple steps further.

## Manipulating Text
To change the text displayed in an HTML element from JavaScript, use the `innerText` method:

```js
element.innerText = "hello";
```
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="poGMYEX" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYEX">
  innerText (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Manipulating Values
Some HTML elements, notably `<button>` and `<input>`, can have a value attribute. This attribute is a way to read, store, or change some information - usually, a number - that is associated specifically with that element.

Take a look at the 3 sliders - `<input>` elements with `type="range"` - in the example below. Each one is written with a different initial value attribute, which is why they all start at different positions (sliders have a range from 0 to 100 by default).
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="OJdKqbw" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/OJdKqbw">
  Input Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
These values can be read in JavaScript (e.g. in response to changes to the slider made by the user), but they can also be set from JavaScript.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abXeMBZ" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abXeMBZ">
  Setting Input Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>