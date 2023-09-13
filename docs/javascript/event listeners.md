---
layout: default
parent: JavaScript
title: Event Listeners
nav_order: 5
---
# Event Listeners
An *event* is a signal that something has happened in the browser. There are several triggers for [events](https://developer.mozilla.org/en-US/docs/Web/Events), some that occur automatically (e.g. the *[load](https://developer.mozilla.org/en-US/docs/Web/API/Window/load_event)* event fires when the whole page has finished loading), and others that occur in response to an interaction from the user (e.g. the *[click](https://developer.mozilla.org/en-US/docs/Web/API/Element/click_event)* event fires when the user clicks on a page element). In this class, we will primarily be focussed on the latter category.

In order to make something happen in response to an event, we need to attach an *[event listener](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener)* to the interactive element in JavaScript.

## Adding an Event Listener
As with many coding scenarios, there are multiple ways to approach browser-based interaction development. For consistency and simplicity, the recommended procedure for this class is as follows:
1. Declare a variable to reference the interactive element
2. Write a function that defines what should happen when the interaction occurs
3. Add an event listener that calls the function

### Declare a variable to reference the interactive element
In addition to the [basic data types](basic data types) that we have already covered (number, string, boolean), a variable can also be assigned to an *HTML element*.
```js
let myButton = document.getElementById('my-button')
```

Notice that the name of this method is "getElementById" - this implies that the element we are trying to reference should have a matching *id* attribute.

```html
<button id="my-button">Click Me</button>
```

Also notice that the naming convention for the id in HTML (and where it is used in getElementById) is *kebab-case*, while the variable name in JavaScript is *camelCase*. In order to prevent any confusion, it is recommended to use the same wording for both the id and the variable name, but styled appropriately (kebab-case or camelCase, based on location in code).

### Write a function that defines what should happen when the interaction occurs
In this simple example, we will log the message 'Button was clicked!' to the console.
```js
function wasClicked() {
  console.log('Button was clicked!')
}
```

### Add an event listener that calls the function
The *event listener* should be added to the element that fires the desired event - in this case, *the element that the user interacts with*, which is a button. As previously mentioned, there are many different kinds of events that can be listened for - we will specifically be listening for the *click* event.

```js
myButton.addEventListener('click', wasClicked)
```

Notice that this statement begins with the variable name that we created in step 1. The *addEventListener* method is given 2 arguments: the event type to listen for ('click)', followed by the name of the function we created in step 2 (wasClicked).

Try forking the embedded example below and clicking the button - remember, you'll need to open the Replit console in order to see the results logged to the console.

<iframe src="https://replit.com/@sheffie/IMS322-Event-Listener?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>