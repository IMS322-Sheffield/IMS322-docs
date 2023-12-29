---
layout: default
title: Optimizing Images
---
# Optimizing Images
Ensure that all image files used in your projects are reasonably sized (not too large, not too small) according to their intended use.

You should consider how much of the browser window your images will cover (in pixels), and then *double that value* when cropping or downloading image files. For example, an image that will only take up half of the browser window at the most (e.g. one side of a two-column layout, `550px` of window space) should have an original width of approximately `1100px`.

When downloading images from [Unsplash](https://unsplash.com), the most appropriate size for your layout will often be the small or medium option. If you do not have the option of downloading the appropriate size (or are starting with a photo from a different source that is too large), use a photo editing application or the online utility [Squoosh](https://squoosh.app) to resize it.
### Image containers and aspect ratios
It is highly recommended to wrap all images in a `<div>` (when it is part of another component, like the logo in a header) or `<figure>` (when the image is self-contained) element. This will generally make it much easier to attain the desired image size and position within your layout without distorting the aspect ratio. All `<img>` elements have the `width: 100%` property applied by default in `ims322-style.css`, which means that they will automatically take on the width of their parent container without becoming stretched or squished. As an added bonus, the `<figcaption>` element can be used inside of a `<figure>` element to easily add captions to your images if desired.
#### Example HTML
```html
<div class="ostrich-container">
  <img src="images/ostrich.jpg" alt="an ostrich">
</div>
```
#### Example CSS
```css
img {
  max-width: 100%;
  max-height: 100vh;
}
```
#### Results
<div style="display: flex; justify-content: center;"> 
  <div style="max-width: 100%; max-height: 100vh;">
	<img src="images/ostrich.jpg" style="width: 100%;">
  </div>
</div>