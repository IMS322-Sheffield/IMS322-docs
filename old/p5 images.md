---
layout: default
title: Images in P5
---
# Images in P5
Images should be loaded inside the [`preload()`](https://p5js.org/reference/#/p5/preload) function to ensure that the files are ready before the `setup()` and `draw()` functions run. Once that is done, the image itself can be drawn to the canvas using the [`image()`](https://p5js.org/reference/#/p5/image) method. As always, maintaining the correct aspect ratio is important and might be best achieved by cropping and/or resizing photos beforehand.
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="VwRZmrv" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/VwRZmrv">
  P5 Images (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>