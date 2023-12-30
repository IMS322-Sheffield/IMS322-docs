# Operators
In previous examples, we have already used 2 operators that have fairly obvious functions: `+` for addition and `=` for assigning values, as seen in the expression:
```js
let y = x + 10;
```

Many other JavaScript operators are similarly self-explanatory, though there are a few useful ones that you may not be familiar with.
## Arithmetic Operators
The standard arithmetic operators are addition `+`, subtraction `-`, multiplication `*`, and division `/`.

The following table lists some of the other useful arithmetic operators provided in JavaScript:

| Operator | Description | Example |
| ----------- | ----------- | ----------- |
| `%` remainder | Returns the remainder of dividing the two operands. | 24 % 7 returns 3, because 24 / 7 is equal to 21 with a remainder of 3. |
| `++` increment | Adds one to its operand. | If `x` is 3, then `x++` sets `x` to 4. |
| `--` decrement | Subtracts one from its operand. | If `x` is 3, then `x++` sets `x` to 2. |

## Assignment Operators
The simple assignment operator is equal `=`, which assigns the value of its right operand to its left operand. That is, `let x = 7` sets the value of x to the number 7.

The following table lists some of the useful compound assignment operators that act as shorthand for the operations in the right column:

|Name|Shorthand|Meaning|
|---|---|---|
|Addition assignment|`x += 7`|`x = x + 7`|
|Subtraction assignment|`x -= 7`|`x = x - 7`|
|Multiplication assignment|`x *= 7`|`x = x * 7`|
|Division assignment|`x /= 7`|`x = x / 7`|
|Remainder assignment|`x %= 7`|`x = x % 7`|

## String Concatenation
When working with strings, `+` acts as the *concatenation* operator, which joins strings together. String concatenation can be used to insert variable values into longer messages.
```js
let myName = "Eric";

console.log("Welcome, " + myName + ".");

// logs "Welcome, Eric."" to the console
```

Try forking the embedded example below and changing the code in the `script.js` file to practice with operators - remember, you'll need to open the Replit console in order to see the results logged to the console.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="WNmeoZX" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/WNmeoZX">
  Operators (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>