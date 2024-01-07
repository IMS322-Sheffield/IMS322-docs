# Advanced Functions
...
## Passing Parameters Into Functions
In the previous example, our function declaration acted essentially as a shorthand for running multiple steps - each time `makeSauce()` was called, it performed 3 individual `console.log()` operations. It should be obvious that even if you only need to "make sauce" a few times, you will end up writing less code in the long run if you first take the time to declare the `makeSauce()` function.

One thing that can make your functions much more flexible and powerful is to define them with one or more *parameters*. Then, you can pass data into the function by providing them as *arguments* when the function is called.

Here is an example that accepts 2 arguments:
```js
function calculateAge(present, past) {
  let currentAge = present - past;
  console.log(currentAge);
}
```
The parameters defined in that function, `present` and `past`, act as local variables within the function - meaning that they are only accessible within the `calculateAge()` function (more on that [below](#variable-scope)).

When calling the function, the values that you wish to use can be passed in as arguments:
```js
calculateAge(2023, 1981);
```

You can also pass variables as arguments:
```js
let currentYear = 2023;
let birthYear = 1981;

calculateAge(currentYear, birthYear);
```

Try forking the embedded example below and changing the code in the `script.js` file - remember, you'll need to open the Replit console in order to see the results logged to the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="jOJNVyY" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/jOJNVyY">
  Function Parameters (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Returning Data From Functions
So far, we have logged results directly to the console from within the functions. There may be cases where you want to use the results somewhere else in your code. To do so, you can *return* data from a function - often, the easiest way to use the returned data is to assign it to a variable first.
```js
let sum = calculateSum(4, 5);

console.log(sum);

function calculateSum(x, y) {
  return x + y;
}
```
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="JjzPbEq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/JjzPbEq">
  Function Return (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>
## Variable Scope
It was mentioned above that the parameters in your function declaration act as *local* variables, which means they can only be accessed from certain parts of the code. Specifically, a variable is only available *within the block of code it was declared*. By "block of code," we mean the contents inside curly braces.

This will work: 
```js
calculateSum(40, 2)

// this function is a block of code -
// because of the curly braces
function calculateSum(x, y) {
  let sum = x + y
  console.log(sum) 
}
```

This will not:
```js
calculateSum(40, 2);

// we're trying to use the variable "sum" here
console.log(sum);

function calculateSum(x, y) {
  // but it is declared here within a set of curly braces
  let sum = x + y;
}
```

This is one reason why understanding the return process is valuable:
```js
let result = calculateSum(40, 2);

console.log(result);

function calculateSum(x, y) {
  let sum = x + y;
  return sum;
}

```

While variables declared inside of a set of curly braces cannot be accessed from outside the curly braces, you CAN work the other way around - *outer* variables (sometimes called *global* variables) can be accessed from deeper levels of curly braces.
```js
let value1 = 40;
let value2 = 2;

function calculateSum() {
  // this will work because value1 and value2 were
  // defined outside of this block of code
  console.log(value1 + value2);
}
```

This relationship will likely become clearer later in the semester when we start writing *conditionals* and *for loops* (which both use curly braces) inside of functions.

The recommendation for this class is to try and minimize the use of outer variables as much as possible. This can usually be accomplished with the proper us of function parameters and return.