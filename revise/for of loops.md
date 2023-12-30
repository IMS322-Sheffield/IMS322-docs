# For Of Loops
Arrays are an example of something that is an *iterable* - this means that we can *iterate* over all of the values of an array with a `for...of` loop.

```js
for (const variable of iterable) {
  // do something for as many times as there are values in the sequence
}
```

In the example presented above, the word "iterable" would be the source of the sequence of values e.g. the variable name of your array. The word "variable" becomes a temporary variable within the loop that receives a value from the sequence on each iteration. 

This can be a little tricky to picture mentally, so let's walk though this example:
```js
let myArray = [12, 34, 56, 78];

for (const m of myArray) {
  console.log(m);
}
```
In this case, the source of the sequence is the variable *myArray*. The `for of` loop will run 4 times because there are 4 values in the myArray sequence. Each time the loop runs, *m* will represent the value of each successive value in the array, starting at `12`, then `34`, then `56`, etc.

Why did we call the temporary variable *m*? Any name can be used, though it is common to see the first letter of the name of the array used as the name for the temporary variable.

Try forking the embedded example below and changing the values within the array in the `script.js` file. Observe the changes in the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="poYzNNa" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poYzNNa">
  For Of Loops (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>