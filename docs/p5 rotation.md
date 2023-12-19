---
layout: default
title: Rotation in P5
---
# Rotation in P5
Rotation (and translation) in P5 are a bit strange. Transformations are not applied to individual shapes, but rather on the *entire canvas.* This means that rotated shapes will generally be drawn in between the [`push()`](https://p5js.org/reference/#/p5/push) and [`pop()`](https://p5js.org/reference/#/p5/pop) methods.

Think of `push()` and `pop()` as though they are a way to draw items to an "offscreen" movable canvas without disrupting the current canvas. Rotating a single shape then requires the following steps:
- `push()` to start the "offscreen" drawing
- [`translate()`](https://p5js.org/reference/#/p5/translate) to move the "offscreen" canvas origin point (0, 0) to the location of the shape that you would like to rotate.
- [`rotate()`](https://p5js.org/reference/#/p5/rotate) to rotate the "offscreen" canvas by the desired amount.
  - *The default mode for rotation uses radians instead of degrees. PI is the equivalent of 360deg, HALF_PI or PI/2 is the equivalent of 180deg, etc.*
- Draw the shape at the origin point (0, 0) of the "offscreen" canvas.
- `pop()` to finish the "offscreen" drawing and return to the normal drawing mode.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="poYzNaK" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/poYzNaK">
  P5 Rotation (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>