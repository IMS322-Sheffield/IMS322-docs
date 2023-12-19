---
layout: default
title: Advanced CSS
---
# Advanced CSS
The topics on this page are not necessarily complex but are being categorized as "advanced" since they might not have been covered in all sections of IMS222. We will cover these topics as needed during the first few weeks of the semester, pending the results of the IMS322 Review Survey (the first assignment in Canvas). Below, you will find brief descriptions and embedded examples for each topic.
## Relative units
As noted on the [Review](review.md#relative-units) and [Style Guide](style-guide.md#use-flexible-and-relative-units-whenever-possible) pages, using relative units by default will often make layout spacing and element sizing more consistent and flexible. In the embedded example below, each `<p>` has been sized using one of the relative units recommended for this class:
- `%` - Percentage relative to the parent element. 
- `ch` - The width of the number "0" of the element's font.
- `rem`	- Relative to the default browser font size.
- `vw` - 1% of the viewport's (window) width.
- `vh` - 1% of the viewport's (window) height.

Try adjusting the properties in the `style.css` file of this example Repl to see how they affect the resulting dimensions of each `<p>`.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBgevda" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevda">
  Relative CSS Units (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## CSS variables
You can declare CSS variables (aka custom properties) at the top of your `style.css` document in the `:root` pseudo-element. These can then be referenced throughout the rest of the stylesheet by their variable name.

CSS variables help to ensure consistency of custom properties throughout your site (e.g. apply a specific color in multiple places without needing to remember the exact HEX code). They can also make it easier test variations since you only need to change a property where it was initially declared - the change will automatically propagate through every instance where the variable was used.
<p class="codepen" data-height="350" data-default-tab="html,result" data-slug-hash="wvNVOKx" data-editable="true" data-user="ersheff" style="height: 350px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/wvNVOKx">
  CSS Variables (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## :hover pseudo-class
A "pseudo-class" keyword is added to a selector to specify different styling properties for a special state of the selected elements. The keyword that you will likely use most often is `:hover`. Adding `:hover` to the end of an existing class defines how that element should be styled when it is hovered over. Usually, this is just a variation of the original style, like a slight color change.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="abXeMdN" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/abXeMdN">
  :hover (IMS322 docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
## Transition times
Setting a transition time (in seconds) causes changes between two states to happen gradually. The example below demonstrates a transition time using the `:hover` pseudo-class to initiate a change, but these changes can also originate from JavaScript.
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="qBgevZq" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/qBgevZq">
  CSS Transitions (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>