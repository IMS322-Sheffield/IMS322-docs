---
layout: default
title: Arrays
---
# Arrays
Individual bits of data, whether number or strings, often gain more meaning when they are presented in context with other data. For example, the latitude of the Miami University campus is **39.508930578260085**. It would be very difficult to locate the campus using GPS coordinates without the corresponding longitude of **-84.73448077561027**. Similarly, if you want to discover [trends in enrollment at Miami University](https://miamioh.edu/oir/data/factbook/enrollment-undergraduate/index.html) you'll need to look at several years' worth of data simultaneously in order to get a clear picture.

In JavaScript, an *array* is a type of variable specially suited to store sequences of values. An array is declared just like any other value variable with the keyword `let`. The values of the array are surrounded by square brackets and separated by commas.
```js
let myArray = [12, 34, 56, 78];
```

To read out a single value from the array, you refer to it by the *index*, which is the location within the array, starting at 0. For example, given myArray above...
```js
myArray[0];
```
would return the first value: `12`.

Try forking the embedded example below and changing the values within the array and the index number in the `script.js` file.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="PoVMLNe" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLNe">
  Arrays (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>