# Canvas Responsiveness
Making your P5 canvas responsive require a combination of:
- [`windowWidth`](https://p5js.org/reference/#/p5/windowWidth) and [`windowHeight`](https://p5js.org/reference/#/p5/windowHeight) variables, which return the current dimensions of the browser window
- [`windowResized()`](https://p5js.org/reference/#/p5/windowResized) function, which runs when the window has been resized
- [`resizeCanvas()`](https://p5js.org/reference/#/p5/resizeCanvas) method, which resizes the canvas (usually run from within the `windowResized` function)
<p class="codepen" data-height="300" data-default-tab="js,result" data-slug-hash="RwdboQR" data-editable="true" data-user="ersheff" style="height: 300px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;">
  <span>See the Pen <a href="https://codepen.io/ersheff/pen/RwdboQR">
  P5 Responsiveness (IMS322 Docs)</a> by Eric Sheffield (<a href="https://codepen.io/ersheff">@ersheff</a>)
  on <a href="https://codepen.io">CodePen</a>.</span>
</p>
<script async src="https://cpwebassets.codepen.io/assets/embed/ei.js"></script>