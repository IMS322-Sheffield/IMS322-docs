---
layout: default
title: CSS Nesting
parent: CSS
---
# CSS Nesting
Excerpted from MDN Web Docs ["Using CSS nesting"](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Using_CSS_nesting):

> \[CSS Nesting\] allows you to write your stylesheets so that they are easier to read, more modular, and more maintainable. As you are not constantly repeating selectors, the file size can also be reduced.

> You can use CSS nesting to create child selectors of a parent, which in turn can be used to target child elements of specific parents.

While nesting may not be appropriate for all situations, a notable benefit is that the structure more closely resembles the corresponding HTML - meaning that children inside parent elements can be styled with child selectors inside parent selectors. 

*Previously, this required adding the [`&` nesting selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Nesting_selector) in front of the child selector. However, the most recent versions of all common browsers have been updated to support nesting without the `&`, which makes it a little easier to write.*

```css
parent {
  /* parent styles */
  
  child {
    /* child of parent styles */
  }
}
```
<p class="codepen" data-height="300" data-default-tab="html,result" data-slug-hash="PoVMLGa" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/PoVMLGa">
  CSS Nesting (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>