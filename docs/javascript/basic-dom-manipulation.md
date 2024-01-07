---
layout: default
title: Basic DOM Manipulation
parent: JavaScript
---
# Basic DOM Manipulation
Although JavaScript was designed as the programming language of the web, HTML and JavaScript are different languages. JavaScript cannot understand HTML the way that it is written.

For example, this is not valid JavaScript:
```js
let mainHeading = <h1>Welcome</h1>;
```

The Document Object Model, or DOM, is the "representation of the objects that comprise the structure and content of a document on the web." You can think of the DOM as a translation of HTML that JavaScript can understand. It defines:

1. The HTML elements as objects (the way an HTML element is treated when assigned to a variable).
```js
let mainHeading = document.getElementById("main-heading");
```
  2. The properties (values or attributes) of HTML elements. Properties can typically be recognized because they appear after a variable name, separated by a `.`
```js
headshotImage.src = "images/headshot.webp";
```
3. The methods (actions) that can be performed on or by HTML elements. Methods can typically be recognized because they appear after a variable name, separated by a `.`, with `()` at the end. Many (but not all) methods require an argument inside the `()` to be passed to the method.
```js
primaryButton.classList.toggle("active");
```
4. The events that can be fired by HTML elements.
```js
primaryButton.addEventListener("click", toggleState);
```

## Getting Started with Properties
### innerText
To change the text displayed in an HTML element from JavaScript, assign the `innerText` property to the desired value:
```js
element.innerText = "Hello!";
```
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="poGMYEX" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYEX">
  innerText (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
### Values
Some HTML elements, notably `<input>`, have a value attribute which can be read or assigned as a property in JavaScript.

Take a look at the 4 sliders below. Each one is give a different initial value attribute in the HTML, which is why they all start at different positions (sliders have a range from 0 to 100 by default).
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="OJdKqbw" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/OJdKqbw">
  Input Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
These values can be read in JavaScript (e.g. in response to changes to the slider made by the user), but they can also be set from JavaScript.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abXeMBZ" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abXeMBZ">
  Getting and Setting Values (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Getting Started with Methods
  Some methods - like `document.getElementById()`, `console.log()`, `.addEventListener()`, and `classList.toggle()` - get used so frequently that they become second nature. Sometimes you may need to reference online documentation in order to discover the methods (and properties and events) associated with an object. For example, the `play()` method is mentioned in the [Basic Usage](https://developer.mozilla.org/en-US/docs/Web/API/HTMLAudioElement#basic_usage) section of the MDN Web Docs article on HTML Audio Elements.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="vYPGjPy" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/vYPGjPy">
  Audio Element Methods (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>