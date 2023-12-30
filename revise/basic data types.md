# Basic Data Types
Values stored in [variables](variables.md) are always of a certain *type*. Being aware of these types is important when developing your code as they determine what you can do with that data.

If you were prompted to "add 40 and 2 in your head," you could easily do so because 40 and 2 are both of the type "number." However, a request to "add 40 and elephant" does not have an obvious response because we don't typically add numbers to animals. Outside of creative nonsense answers - "uhh... fortyphant?" - it doesn't make any sense.

Data types in JavaScript work in a similar manner. If you try to manipulate data in a way that is expected *given the types* (e.g. add two numbers together), you should get a logical response. If you try to manipulate data in ways that are not expected *given the types* (e.g. add numbers to words), then you will either receive a creative nonsense answer or an error.

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

Try forking the embedded example below and changing the code in the `script.js` file - remember, you'll need to open the Replit console in order to see the results logged to the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="poGMYym" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poGMYym">
  Data Types (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## "Null" and "undefined"
It is unlikely that you will ever intentionally assign a value of "null" or "undefined" to a variable while in this class (though you may find reasons to do so in the future). However, it's important to know about these two special values because there's a significant chance that they will appear as part of an error message in the console.

*Null* essentially means "empty" (which is not the same as the numerical value of 0).

*Undefined* essentially means "does not exist" or "not assigned". If you see an error in the console that says something is undefined, there's a good chance that you're trying to work with a variable that was never assigned a value or a property that an object does not have.
<div style="display: flex; justify-content: center;"> 
  <figure style="max-width: 500px;">
	  <img src="images/values.png" style="width: 100%;">
	  <figcaption style="font-style: italic; text-align: center;">Original image source unknown - duplicated from <a href="https://deepak7jha.medium.com/javascript-null-undefind-93b443cc924e">Medium</a></figcaption>
  </figure>
</div><script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>