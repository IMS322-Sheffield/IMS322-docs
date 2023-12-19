---
layout: default
title: More Controls
---
# More Controls
The simplest form of control or input type typically presented to the user is the button. It presents only a binary choice - to click or not to click. No other information or decision-making is required.

There are many other input types that vary in complexity and application. It is important that the type of input is a good fit for the information that is being collected. For example, the default text input is too generic for entering a date, while a dropdown menu or multiple-choice style radio button is impractical when there is a very large number of possible or valid answers.

Like many concepts in this class, it is a good idea to familiarize yourself with the curated collection of controls presented in the examples below. A full reference for all input types can be found [here](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input).

## Selection Controls
A selection control allows the user to choose from a group of valid choices. The type of selection controls presented in the example below are radio buttons. Radio buttons are typically best for multiple-choice style questions in which only one option is selectable.

Some important things to note about radio buttons:
- While not required, it is recommended to put radio buttons in a `<fieldset>` element to visually and semantically group them.
- The `name` attribute given to the radio buttons is what binds them to each other so that only one can be selected at a time.
- Each radio button is paired with a `<label>` element to provide text instructions or descriptions. The `for` attribute of each `<label>` should be the same as the `id` or the corresponding input.
- The `value` attribute is what will typically be gathered in your JavaScript. This does not need to be the same as the `<label>` text.
- It can be a little tricky to find selected radio buttons in JavaScript. The recommendation for this class is to use `document.querySelector("input[type='radio']:checked")`.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="XWGrNgo" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/XWGrNgo">
  Selection Controls (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## List Controls
List controls allow users to select from a finite set of text strings, each representing a command, object, or attribute. The dropdown menu list control demonstrated in the example below is (somewhat confusingly) created using the `<select>` element. Each item in the dropdown menu is created by adding `<option>` elements.

Some important things to note about `<select>` dropdown menus:
- Like radio buttons, the `value` attribute is what will typically be gathered in your JavaScript. This does not need to be the same as the displayed text.
- With this and most other inputs and controls, you can go back to using `document.getElementById()` to assign the element to a variable in JavaScript.
- It is recommended to put instructions in the first `<option>` with an empty `value` since it will be the first thing the user sees.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="dyrbOzP" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/dyrbOzP">
  List Controls (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Entry Controls
Entry controls enable users to supply information to or set a value in an application. The most basic entry control is the `<input>` element with default type `text`. However, other types may be better suited to different types of data. For example, the `date` type provides a dropdown calendar and automatic `mm/dd/yy` formatting, while the `number` type adds increment and decrement buttons with an easy way to set minimum and maximum attributes.

The `placeholder` and `value` attributes of entry controls can be very useful - placeholder text can provide instructions or hints without the need for a separate `<label>`, while setting the `value` attribute in HTML provides a default value.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="yLwBVoE" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/yLwBVoE">
  Entry Controls (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>