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

<iframe src="https://replit.com/@sheffie/IMS322-Arrays?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>