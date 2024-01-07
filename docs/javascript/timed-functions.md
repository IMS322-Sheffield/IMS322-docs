---
layout: default
title: Timed Functions
parent: JavaScript
---
# Timed Functions
There are often instances where your application requires something to occur at a regular time interval regardless of user activity. Some examples include:
- An autosave function that automatically saves the user's work every 5 minutes.
- A timer that reports elapsed time while taking a quiz.
- An app that automatically checks the internet for new Taylor Swift news every minute.

In these scenarios, the `setInterval()` method can be used to repeatedly call a function with a specific delay between each call.

## setInterval()
Writing functions to be called by `setInterval()` is no different than writing them for other methods (like event listeners). The difference is primarily in how the function is called.
```js
setInterval(function, delay);
```

The delay is expressed in milliseconds, so `1000` is equivalent to 1 second.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="qBvWqoB" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBvWqoB">
  setInterval Random (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
In the example below, the `setProperty()` method is introduced as a way to manually change a single style property from JavaScript.  You should aim to use class toggling to change styling whenever possible. However, `setProperty()` is required if you want to provide different values depending on other conditions.
```js
element.style.setProperty(propertyName, value);
```
The `propertyName` argument can be any familiar CSS styling property formatted as a string, like `"background-color"` or `"font-size"`. For `value`, you will usually need to use string concatenation to append units e.g. add `"px"` or `"rem"` to the end of a number.

The `shift` function is called every second to randomly move the text by changing the `translate` property, while the `spin` function is called every 10ms to continuously rotate the bar. Notice how `"px"` and `"deg"` are concatenated to the variables in JavaScript before they are passed as arguments to `setProperty()`.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="KKEPNoe" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/KKEPNoe">
  setInterval with setProperty (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>