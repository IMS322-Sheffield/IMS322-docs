---
layout: default
parent: Combination
title: Input Validation
nav_order: 3
---
# Input Validation
When using entry controls, it is a good idea to validate the input to ensure that it adheres to the desired format or range of valid answers. For example, a first or last name typically should not include numbers, dates in the mm/dd/yy format should not include letters, and required inputs should not be submitted empty.
## HTML Form Validation
The good news is that many `<input>` types will automatically validate data for their given type and attributes if they are put inside of a `<form>` element with a corresponding Submit button.

In the example below:
- The first text input is given the `required` attribute, so it cannot be empty.
- The email input will not accept data if it is not in the typical user@domain.com format since it has the `email` type attribute.
- The date input will not allow letters to be typed in, only numbers.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="bGzXObb" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/bGzXObb">
  Quick Validation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>

Further customization can be attained by using `minlength` and `maxlength` attributes for text strings and `min` and `max` attributes for numerical input types. The `pattern` attribute provides an extensive amount of control over the exact formatting of text entry, BUT it must be written as a [regular expression](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) (regex), which can be very challenging to design yourself. A simple example that only accepts letters and spaces is shown below, but beyond that you might need to resort to searching for example regex online.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="RwvXEbq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwvXEbq">
  RegEx Validation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## JavaScript Validation
If you want more control over the look and feel of the native error messages provided by the HTML Form Validation demonstrated above, you must use JavaScript.

- `element.validity.typeMismatch` will return `true` if the value is not in the required syntax according to its type.
- `element.validity.valueMissing` will return `true` if the field is empty and the input has the `required` attribute set.
- `emailEntry.setCustomValidity('message here')` allows for custom validation messages.

There are a few other options for JavaScript input validation described [here](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#validating_forms_using_javascript), though the methods that will most likely prove useful in this class are demonstrated below.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="yLZmGLJ" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/yLZmGLJ">
  JavaScript Validation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>