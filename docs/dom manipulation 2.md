---
layout: default
title: DOM Manipulation 2
---
# DOM Manipulation 2 - Style Properties
The recommended way to change visual states is to use [class toggling](class toggle) with the `classToggle()` method. However, this really only works when alternating between 2 different states. What if you want to manage more than 2 states? Or what if you want continuously variable control of a style property?

The `style.setProperty()` method can help to address these other scenarios.

```js
element.style.setProperty("property-name", "value");
```

The `"property-name"` string can be any familiar CSS styling property, like `"background-color"` or `"font-size"`. For `"value"`, don't forget to include the units if needed. You may have to use string concatenation e.g. add `"px"` or `"rem"` to the end of a variable or number.

<iframe src="https://replit.com/@sheffie/IMS322-DOM-Style-Properties?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>