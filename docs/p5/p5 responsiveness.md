---
layout: default
title: Canvas Responsiveness
parent: P5
nav_order: 1
---
# Canvas Responsiveness
Making your P5 canvas responsive require a combination of:
- [`windowWidth`](https://p5js.org/reference/#/p5/windowWidth) and [`windowHeight`](https://p5js.org/reference/#/p5/windowHeight) variables, which return the current dimensions of the browser window
- [`windowResized()`](https://p5js.org/reference/#/p5/windowResized) function, which runs when the window has been resized
- [`resizeCanvas()`](https://p5js.org/reference/#/p5/resizeCanvas) method, which resizes the canvas (usually run from within the `windowResized` function)

<iframe src="https://replit.com/@sheffie/IMS322-P5-Responsiveness?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>