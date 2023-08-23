---
layout: default
title: Advanced CSS
parent: CSS
nav_order: 2
---
# Advanced CSS
The topics on this page are not necessarily complex but are being categorized as "advanced" since they might not have been covered in all sections of IMS222. We will cover these topics as needed during the first few weeks of the semester, pending the results of the IMS322 Review Survey (the first assignment in Canvas). Below, you will find brief descriptions and embedded examples for each topic.
## Relative units
As noted on the [Review](docs/general/review#relative-units) and [Style Guide](docs/general/style-guide#use-flexible-and-relative-units-whenever-possible) pages, using relative units by default will often make layout spacing and element sizing more consistent and flexible. In the embedded example below, each `<p>` has been sized using one of the relative units recommended for this class:
- `%` - Percentage relative to the parent element. 
- `ch` - The width of the number "0" of the element's font.
- `rem`	- Relative to the default browser font size.
- `vw` - 1% of the viewport's (window) width.
- `vh` - 1% of the viewport's (window) height.

Try adjusting the properties in the `style.css` file of this example Repl to see how they affect the resulting dimensions of each `<p>`.
<iframe src="https://replit.com/@sheffie/IMS322-Relative-Units?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
## CSS variables
You can declare CSS variables (aka custom properties) at the top of your `style.css` document in the `:root` pseudo-element. These can then be referenced throughout the rest of the stylesheet by their variable name.

CSS variables help to ensure consistency of custom properties throughout your site (e.g. apply a specific color in multiple places without needing to remember the exact HEX code). They can also make it easier test variations since you only need to change a property where it was initially declared - the change will automatically propagate through every instance where the variable was used.
<iframe src="https://replit.com/@sheffie/IMS322-CSS-Variables?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
## :hover pseudo-class
A "pseudo-class" keyword is added to a selector to specify different styling properties for a special state of the selected elements. The keyword that you will likely use most often is `:hover`. Adding `:hover` to the end of an existing class defines how that element should be styled when it is hovered over. Usually, this is just a variation of the original style, like a slight color change.
<iframe src="https://replit.com/@sheffie/IMS322-Hover?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
## Transition times
Setting a transition time (in seconds) causes changes between two states to happen gradually. The example below demonstrates a transition time using the `:hover` pseudo-class to initiate a change, but these changes can also originate from JavaScript.
<iframe src="https://replit.com/@sheffie/IMS322-Transition?embed=true" width="100%" height="480" style="border: none; border-radius: 8px; box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);"></iframe>
