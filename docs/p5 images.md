---
layout: default
title: Images in P5
---
# Images in P5
Images should be loaded inside the [`preload()`](https://p5js.org/reference/#/p5/preload) function to ensure that the files are ready before the `setup()` and `draw()` functions run. Once that is done, the image itself can be drawn to the canvas using the [`image()`](https://p5js.org/reference/#/p5/image) method. As always, maintaining the correct aspect ratio is important and might be best achieved by cropping and/or resizing photos beforehand.

<iframe src="https://replit.com/@sheffie/IMS322-P5-Images?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>