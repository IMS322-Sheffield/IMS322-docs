---
layout: default
title: Flexbox
parent: CSS
---
# Flexbox
Flexbox is used to create responsive layouts. It is typically best for 1-dimensional rows or columns, though more complex layouts can be achieved by nesting flexboxes inside of each other.

From [CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/):
> The main idea behind the flex layout is to give the container the ability to alter its items’ width/height (and order) to best fill the available space (mostly to accommodate to all kind of display devices and screen sizes). A flex container expands items to fill available free space or shrinks them to prevent overflow.

<div style="display: flex; justify-content: space-evenly; gap: 1ch;">
	<div style="flex: 1; max-width: 350px">
		<img src="../images/01-container.svg" style="width: 100%">
	</div>
	<div style="flex: 1; max-width: 350px">
		<img src="../images/02-items.svg" style="width: 100%">
	</div>
</div>
The CSS Tricks article linked above is an excellent reference for all things flexbox. From that article, there are 7 key properties that can be used to accomplish most layout goals:
- Container properties:
  - `display` - Set to `flex` to define a flex container (create a flexbox).
  - `flex-direction` - Set to `row` (the default) or `column`.
  - `flex-wrap` - By default, flexbox will try to fit everything in one row or column. Set this property to `wrap` to wrap flex items to multiple lines (only works if items have a fixed or minimum size).
  - `justify-content` - Defines the alignment along the main axis.
  - `align-items` - Defines the alignment along the cross axis.
  -  `gap` - Controls the space between flex items.
- Item properties:
  - `flex` - Determines how much space an item will inhabit proportionally. For example, a flex item with `flex: 2` will take up twice as much space as a flex item with `flex: 1` (demonstrated in the first flexbox below).
<p class="codepen" data-height="600" data-default-tab="html,result" data-slug-hash="VwRLgEg" data-editable="true" data-user="ersheff" style="height: 600px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/VwRLgEg">
  Flexbox (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>