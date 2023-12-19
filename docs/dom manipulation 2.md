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
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBgevRR" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevRR">
  Changing Style Properties (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>