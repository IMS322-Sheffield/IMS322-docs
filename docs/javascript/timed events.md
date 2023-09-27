---
layout: default
parent: JavaScript
title: Timed Events
nav_order: 10
---
# Timed Events
There are often instances where your design requires something to occur at a regular interval rather than being driven by user interaction:
- An autosave function that saves the user's work every 5 minutes
- A timer readout that reports elapsed time in seconds since a quiz was started
- An app that automatically checks the internet for new Taylor Swift news every minute

In these scenarios, the `setInterval()` method can be used to repeatedly call a function with a fixed time delay between each call.

## setInterval()
Writing functions to be called by `setInterval()` is no different than writing them for event listeners. The primary distinction is in determining *why* or *how* you need your function to be called:
- If the function should be called when a user interaction has occurred - pressing a button, moving a slider, entering text in a text field, etc. - use an event listener.
- If the function should be called automatically every X seconds, use `setInterval()`.

The format to use with `setInterval()` is:
```js
setInterval(function, delay)
```

The delay is expressed in milliseconds - so, `1000` is equivalent to 1 second.

<iframe src="https://replit.com/@sheffie/IMS322-setInterval-Random?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>

In the example below, the `setProperty()` method is introduced as a way to manually change a single style property from JavaScript. The format for using `setProperty()` is:

```js
element.style.setProperty('property-name', 'value')
```

The `'property-name'` string can be any familiar CSS styling property, like `'background-color'` or `'font-size'`. For `'value'`, don't forget to include the units if needed. You may have to use string concatenation e.g. add `'px'` or `'rem'` to the end of a variable or number.

In the example below, the `translate` property is used to randomly move the text every second. Notice how `'px'` is concatenated to the random value in JavaScript.

<iframe src="https://replit.com/@sheffie/IMS322-setInterval-setProperty?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>