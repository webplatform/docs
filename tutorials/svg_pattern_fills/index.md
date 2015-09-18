---
title: 'SVG pattern fills'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/en-US/docs/SVG/Tutorial/Patterns)'
readiness: 'Ready to Use'
summary: 'This article covers SVG pattern fills.'
tags:
  - Tutorials
  - SVG
uri: 'tutorials/svg pattern fills'

---
## Summary

This article covers SVG pattern fills.

Patterns, in my opinion, are one of the more confusing fill types to use in SVG. They're also very powerful, so they're worth talking about and getting at least a fundamental grasp on. Like gradients, the `<pattern>` element should be put in the `<defs>` section of your SVG file.

![SVG Pattern Example.png](//static.webplatform.org/3/3d/SVG_Pattern_Example.png)

    <?xml version="1.0" standalone="no"?>
    <svg width="200" height="200" xmlns="http://www.w3.org/2000/svg" version="1.1">
      <defs>
        <linearGradient id="Gradient1">
          <stop offset="5%" stop-color="white"/>
          <stop offset="95%" stop-color="blue"/>
        </linearGradient>
        <linearGradient id="Gradient2" x1="0" x2="0" y1="0" y2="1">
          <stop offset="5%" stop-color="red"/>
          <stop offset="95%" stop-color="orange"/>
        </linearGradient>

        <pattern id="Pattern" x=".05" y=".05" width=".25" height=".25">
          <rect x="0" y="0" width="50" height="50" fill="skyblue"/>
          <rect x="0" y="0" width="25" height="25" fill="url(#Gradient2)"/>
          <circle cx="25" cy="25" r="20" fill="url(#Gradient1)" fill-opacity="0.5"/>
        </pattern>

      </defs>

      <rect fill="url(#Pattern)" stroke="black" x="0" y="0" width="200" height="200"/>
    </svg>

Inside the pattern element you can include any of the other basic shapes you've included before, and each of them can be styled using any of the styles you've learned before, including gradients and opacity. Here we've just drawn two rectangle elements inside our pattern (which overlap, and one of which is twice the size of the other and is used to fill in the entire pattern), and one circle.

The confusing thing about patterns is defining a unit system and their size. In the example above, we've defined a `width` and `height` attribute on the pattern element, to describe how far the pattern should go before it begins repeating itself again. There are also `x` and `y` attributes available if you want to offset the start point of this rectangle somewhere within your drawing. The reason they've been used here is described below.

As with the `gradientUnits` attribute used above, patterns also have an attribute, `patternUnits` which specifies the units that these attributes will take. It defaults to "objectBoundingBox" as it did above, so a value of 1 is scaled to the width/height of the object you're applying the pattern to. Since, in this case, we wanted the pattern to repeat 4 times horizontally and vertically, the height and width are set to 0.25. That means the patterns width/height is only 0.25 of the total box size.

Unlike gradients, patterns then have a second attribute, `patternContentUnits`, which describes the units system used inside the pattern element, on the basic shapes themselves. This attribute defaults to "userSpaceOnUse", the opposite of the `patternUnits` attribute. What this means is that unless you specify one or both of these attributes (`patternContentUnits` and `patternUnits`), the shapes you draw inside your pattern are being drawn in a different coordinate system than the pattern element is using, which can make things a bit confusing when you're writing this by hand. To make this work in the above example, we had to consider the size of our box (200 pixels) and the fact that we wanted the pattern to repeat itself 4 times horizontally and vertically. That means that each pattern unit was a 50x50 square. The two rects and the circle inside the pattern were then sized to fit in a 50x50 box. Anything that we had drawn outside that box wouldn't have been shown. The pattern also had to be offset by 10 pixels so that it would start in the upper left corner of our box, so the x and y attributes of the pattern had to be adjusted to 10/200 = 0.05.

The caveat here is that if the object changes size, the pattern itself will scale to fit it, but the objects inside will not. So while we would still have 4 repeating units inside the pattern, the objects composing that pattern would remain the same size, and you end up with large areas of nothing in between them. By changing the `patternContentUnits` attribute, we can put all the elements into the same unit system:

    <pattern id="Pattern" width=".25" height=".25" patternContentUnits="objectBoundingBox">
       <rect x="0" y="0" width=".25" height=".25" fill="skyblue"/>
       <rect x="0" y="0" width=".125" height=".125" fill="url(#Gradient2)"/>
       <circle cx=".125" cy=".125" r=".1" fill="url(#Gradient1)" fill-opacity="0.5"/>
     </pattern>

Now, because the pattern content is in the same unit system as the pattern, we don't have to offset the box so that the pattern starts in the correct place, and if the object size was changed to a larger one, the pattern would automatically scale so that it had the same number of objects and repeats inside it. This contrasts with the "userSpaceOnUse" system, where if the object changes size the pattern would stay the same, and just repeat itself more times to fill the box.

As a slight aside, in Gecko circles seem to have trouble drawing if their radius is set to something less than 0.075 (even though they should be scaled up to have a much larger radius than that. This may be a bug in just the pattern element, or not a bug at all, I'm not sure). To work around that its probably best to avoid drawing in "objectBoundingBox" units unless you have to.

Neither of these uses is what one would normally think of when you think of a pattern. Patterns usually have a set size and repeat themselves independently of what an objects shape is. To create something like this, both the pattern and its contents must be drawn in the current userSpace, so that they don't change shape if the object does:

     <pattern id="Pattern" x="10" y="10" width="50" height="50" patternUnits="userSpaceOnUse">
       <rect x="0" y="0" width="50" height="50" fill="skyblue"/>
       <rect x="0" y="0" width="25" height="25" fill="url(#Gradient2)"/>
       <circle cx="25" cy="25" r="20" fill="url(#Gradient1)" fill-opacity="0.5"/>
     </pattern>

![SVG Pattern Comparison of Units.png](//static.webplatform.org/6/6d/SVG_Pattern_Comparison_of_Units.png)

Of course, this means that the pattern won't scale if you change your object size later. All three of the above examples are shown below on a rectangle that has been slightly elongated to a height of 300px, but I should note its not an exhaustive picture, and there are other options available depending on your application.
