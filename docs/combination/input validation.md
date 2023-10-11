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

<iframe src="https://replit.com/@sheffie/IMS322-Quick-Validation?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>

Further customization can be attained by using `minlength` and `maxlength` attributes for text strings and `min` and `max` attributes for numerical input types. The `pattern` attribute provides an extensive amount of control over the exact formatting of text entry, BUT it must be written as a [regular expression](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes/pattern) (regex), which can be very challenging to design yourself. A simple example that only accepts letters and spaces is shown below, but beyond that you might need to resort to searching for example regex online.

<iframe src="https://replit.com/@sheffie/IMS322-Regex-Validation?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>

## JavaScript Validation
If you want more control over the look and feel of the native error messages provided by the HTML Form Validation demonstrated above, you must use JavaScript.

- `element.validity.typeMismatch` will return `true` if the value is not in the required syntax according to its type.
- `element.validity.valueMissing` will return `true` if the field is empty and the input has the `required` attribute set.
- `emailEntry.setCustomValidity('message here')` allows for custom validation messages.

There are a few other options for JavaScript input validation described [here](https://developer.mozilla.org/en-US/docs/Learn/Forms/Form_validation#validating_forms_using_javascript), though the methods that will most likely prove useful in this class are demonstrated below.

<iframe src="https://replit.com/@sheffie/IMS322-JS-Validation?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>