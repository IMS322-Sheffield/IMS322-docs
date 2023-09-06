---
layout: default
title: Basic Data Types
parent: JavaScript
nav_order: 2
---
# Basic Data Types
Values stored in [variables](variables) are always of a certain *type*. Being aware of these types is important when developing your code as they determine what you can do with that data.

For example, if I said to you "add 40 and 2 in your head," you could do that without any problem because 40 and 2 are both of the type "number." However, you would probably think I was trying to cause trouble if I said "add 40 and elephant" because we don't add numbers to animals. Outside of creative nonsense answers ("uhh... fortyphant?"), it doesn't make any sense.

Data types in JavaScript work in a similar way. If you try to manipulate data in a way that is expected *given the types* (e.g. add two numbers together), everything should work just fine. If you try to manipulate data in ways that are not expected for the types (e.g. add numbers to words), then JavaScript will either give you a creative nonsense answer or throw an error and fail to execute the rest of your code.

While you should be aware of data types, you don't have specify data types when declaring variables. JavaScript is a "dynamically typed" language, which means that it will try to assign the type automatically when running your code.
## Number
```js
let myNumber = 42
```
## String
A string is a sequence of one or more text characters. When declaring a variable that is intended to be a string, surround the value with single quotes, as seen below.
```js
let myMessage = 'Hello, my name is Eric.'
```
## Boolean
The boolean type has only 2 possible values - `true` or `false`. Since these are not strings, they do not need single quotes around the value.
```js
let isItRaining = false
```

Try forking the embedded example below and changing the code in the `script.js` file - remember, you'll need to open the Replit console in order to see the results logged to the console.

<iframe src="https://replit.com/@sheffie/IMS322-Data-Types?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
## "Null" and "undefined"
It is unlikely that you'll be assigning the values of "null" or "undefined" to variables while in this class. However, it's important to be aware of these two special values because there's a very good chance that they will show up as part of error messages in the console.

Null essentially means "empty" or "unknown" (which is not the same as the numerical value of 0).

Undefined essentially means "does not exist." If you see an error in the console that says something is undefined, there's a good chance that you're trying to work with a variable that was never assigned a value or a property that an object does not have.

<div style="display: flex; justify-content: center;"> 
  <figure style="max-width: 500px;">
	  <img src="images/values.png" style="width: 100%;">
	  <figcaption>Original image source unknown - duplicated from <a href="https://deepak7jha.medium.com/javascript-null-undefind-93b443cc924e">Medium</a></figcaption>
  </figure>
</div>