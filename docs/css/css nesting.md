---
nav_order: 3
parent: CSS
title: CSS Nesting
layout: default
---
# CSS Nesting
Excerpted from MDN Web Docs ["Using CSS nesting"](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_nesting/Using_CSS_nesting):

 \[CSS Nesting\] allows you to write your stylesheets so that they are easier to read, more modular, and more maintainable. As you are not constantly repeating selectors, the file size can also be reduced.

  You can use CSS nesting to create child selectors of a parent, which in turn can be used to target child elements of specific parents. This can be done with or without the [`&` nesting selector](https://developer.mozilla.org/en-US/docs/Web/CSS/Nesting_selector).

You can think of CSS nesting as a way to limit the scope of styling to only the child elements of specific parents. This is already possible using combinators, but it can be much more practical with nesting.

```css
/* Without nesting selector */
/* Currently does not work in Safari or
some recent versions of Chrome & Firefox! */
parent {
  /* parent styles */
  child {
    /* child of parent styles */
  }
}

/* With nesting selector */
/* Works in all modern browsers */
parent {
  /* parent styles */
  & child {
    /* child of parent styles */
  }
}

/* the browser will parse both of the above as */
parent {
  /* parent styles */
}
parent child {
  /* child of parent styles */
}
```
<iframe src="https://replit.com/@sheffie/IMS322-CSS-Nesting?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>