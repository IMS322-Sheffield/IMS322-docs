---
layout: default
title: For Of Loops
parent: JavaScript
nav_order: 13
---
# For Of Loops
Arrays are an example of something that is an *iterable* - this means that we can *iterate* over all of the values of an array with a `for...of` loop.

```js
for (let variable of iterable) {
  // do something for as many times as there are values in the sequence
}
```

In the example presented above, the word "iterable" would be the source of the sequence of values e.g. the variable name of your array. The word "variable" becomes a temporary variable within the loop that receives a value from the sequence on each iteration. 

This can be a little tricky to picture mentally, so let's walk though this example:
```js
let myArray = [12, 34, 56, 78]

for (let m of myArray) {
  console.log(m)
}
```
In this case, the source of the sequence is the variable *myArray*. The `for of` loop will run 4 times because there are 4 values in the myArray sequence. Each time the loop runs, *m* will represent the value of each successive value in the array, starting at `12`, then `34`, then `56`, etc.

Why did we call the temporary variable *m*? Any name can be used, though it is common to see the first letter of the name of the array used as the name for the temporary variable.

Try forking the embedded example below and changing the values within the array in the `script.js` file. Observe the changes in the console.

<iframe src="https://replit.com/@sheffie/IMS322-For-Of-Loops?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>