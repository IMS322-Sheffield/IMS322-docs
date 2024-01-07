---
layout: default
title: Basic Data Types
parent: JavaScript
---
# Basic Data Types
Values stored in [variables](variables.md) are always of a certain *type*. Being aware of these types is important when developing your code as they determine what you can do with that data.

If you were prompted to "add 40 and 2 in your head," you could easily do so because 40 and 2 are both of the type "number." However, a request to "add 40 and elephant" does not have an obvious response. Outside of creative nonsense answers - "uhh... fortyphant?" - it doesn't make any sense.

In JavaScript, if you try to manipulate data in a way that is expected *given the types* (e.g. add two numbers together), you should get a logical response. If you try to manipulate data in ways that are not expected *given the types* (e.g. add numbers to words), then you will either receive an unexpected answer or an error.

While you need to be aware of data types, you don't have to specify type when declaring variables. JavaScript is a "dynamically typed" language, which means that types are automatically assigned when code is run based on the how the value was assigned.
## Number
```js
let myNumber = 42;
```
## String
A *string* is a sequence of one or more text characters. When declaring a variable that is intended to be a string, surround the value with single quotes, as seen below.
```js
let myMessage = "Hello, my name is Eric.";
```
## Boolean
The *boolean* type has only 2 possible values - `true` or `false`. Since these are not strings, they do not require single quotes around the value.
```js
let isItRaining = false;
```

Try changing the variable values in the JavaScript below - remember, you'll need to open the console in order to see the results.
<p class="codepen" data-height="300" data-default-tab="js" data-slug-hash="poGMYym" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYym">
  Data Types (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## "Null" and "undefined"
It is unlikely that you will ever intentionally assign a value of "null" or "undefined" to a variable while in this class (though you may find reasons to do so in the future). However, it's important to know about these two special values because there's a significant chance that they will appear as part of an error message in the console.

*Null* is a special value that represents an empty or unknown value (which is not the same as the numerical value of 0).

*Undefined* often occurs if a variable is declared but the value is not assigned.

<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>