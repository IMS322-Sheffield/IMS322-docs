---
layout: default
title: Basic Functions
parent: JavaScript
---
# Basic Functions
Functions are reusable blocks of code that are designed to perform a specific task or group of related tasks. You can accomplish a lot in JavaScript without writing your own functions, but they can help prevent writing repetitive code and will be required for some of the workflows in this class.
## Declaring Functions
To use a cooking analogy, think of the function writing process kind of like training a fellow cook to make part of a meal. If you were preparing spaghetti and meatballs alone, you would have to complete all of the steps yourself every time - chop and sauté the vegetables, combine the meatball ingredients, boil the pasta, etc.

What if you could save time by showing your partner how to make the sauce?

First, you would have to teach them all of the steps of the process:
```
1. Chop stuff
2. Sauté and simmer
3. Season to taste
```

But then, in the future, you could simply ask:
```
Can you please make some marinara?
```

In JavaScript, this first part is called *declaring* a function. Start off by using the `function` keyword, give your function a name (follow the naming conventions from our [style guide](../style-guide.md#naming-variables-and-functions)), then follow with parentheses and curly braces. The individual steps of your function go inside of the curly braces.

```js
function makeSauce() {
  console.log("Chop stuff");
  console.log("Sauté and simmer");
  console.log("Season to taste");
}
```

This function declaration can go anywhere in your JavaScript. When you need your function to actually run, you *call* it:
```js
makeSauce();
```

Try changing the JavaScript below - remember, you'll need to open the console in order to see the results.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="oNVvYBv" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/oNVvYBv">
  Function Declaration (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>