---
layout: default
parent: Combination
title: Modals
nav_order: 1
---
# Modals
A modal is a pop-up that appears on top of the current page. It takes complete priority over the page, meaning that it prevents interaction with the underlying page until it is closed.

While our initial thoughts or impressions of "pop-ups" might tend to be rather negative, like any other component, modals can be effective when used sparingly yet effectively.

## The `<dialog>` element
Incorporating modals became much easier with the addition of the `<dialog>` element to the HTML standard. This element automatically positions itself above underlying content and includes default properties and methods that make it fairly easy to use and customize. Additionally, the `<dialog>` element can be styled like any other `<div>`, including border, background-color, box-shadow, and more.

- JavaScript should be used to display the `<dialog>` element. Use the `.showModal()` method to display a modal dialog. The `<dialog>` box can be closed using the `.close()` method.
- The CSS `::backdrop` pseudo-element can be used to style the backdrop of a modal dialog, which is displayed behind the `<dialog>` element when the dialog is displayed using the `.showModal()` method.
- If you have a `<form>` in your `<dialog>` to collect data from the user, you can set the method attribute of your form to `dialog`. This will cause the form to close the dialog when it is submitted. You can also use the `.preventDefault()` method to perform input validation checks before allowing the modal to close automatically when the Submit button is pressed.

All of the concepts listed above are demonstrated in the example embedded below. Try forking the embedded example below and changing the code in the `index.html` and `script.js` files.

<iframe src="https://replit.com/@sheffie/IMS322-Modals?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
