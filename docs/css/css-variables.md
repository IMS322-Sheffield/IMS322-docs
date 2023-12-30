---
layout: default
title: CSS Variables
parent: CSS
---
# CSS Variables
You can declare CSS variables (aka custom properties) at the top of your stylesheet in the `:root` pseudo-element. These can then be referenced throughout the rest of the document by their variable name.

CSS variables help to ensure consistency of custom properties throughout your site (e.g. apply a specific color in multiple places without needing to remember the exact HEX code). They can also make it easier to test variations since you only need to change a property once where it was initially declared - the change will automatically propagate through every instance where the variable was used.
<p class="codepen" data-height="350" data-default-tab="html,result" data-slug-hash="wvNVOKx" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvNVOKx">
  CSS Variables (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>