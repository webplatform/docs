---
title: 'perspective-origin'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/7033692'
compatibility:
  feature: perspective-origin
  topic: css
overview_table:
  '[Initial value](/css/concepts/initial_value)': '`50% 50%`'
  'Applies to': 'Transformable elements.'
  '[Inherited](/css/concepts/inherited)': 'No'
  Media: visual
  '[Computed value](/css/concepts/computed_value)': 'For length, the absolute value; otherwise, a percentage,'
  Animatable: 'No'
  '[CSS Object Model Property](/css/concepts/cssom)': '`perspectiveOrigin`'
  Percentages: 'The size of the bounding box.'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: "The perspective-origin property establishes the origin for the perspective property. It effectively sets the X and Y position at which the viewer appears to be looking at the children of the element. \n"
tags:
  - CSS_Properties
  - CSS
uri: css/properties/perspective-origin

---
## Summary

The perspective-origin property establishes the origin for the perspective property. It effectively sets the X and Y position at which the viewer appears to be looking at the children of the element.

When used with perspective, perspective-origin changes the appearance of an object, as if a viewer were looking at it from a different origin. An object appears differently if a viewer is looking directly at it versus looking at it from below, above, or from the side. Thus, the perspective-origin is like a vanishing point.

The default value of perspective-origin is 50% 50%. This displays an object as if the viewer's eye were positioned directly at the center of the screen, both top-to-bottom and left-to-right. A value of 0% 0% changes the object as if the viewer was looking toward the top left angle. A value of 100% 100% changes the appearance as if viewed toward the bottom right angle.

## Overview table

[Initial value](/css/concepts/initial_value)
:   `50% 50%`

Applies to
:   Transformable elements.

[Inherited](/css/concepts/inherited)
:   No

Media
:   visual

[Computed value](/css/concepts/computed_value)
:   For length, the absolute value; otherwise, a percentage,

Animatable
:   No

[CSS Object Model Property](/css/concepts/cssom)
:   `perspectiveOrigin`

Percentages
:   The size of the bounding box.

## Syntax

-   `perspective-origin: <length>`
-   `perspective-origin: <percentage>`
-   `perspective-origin: bottom`
-   `perspective-origin: center`
-   `perspective-origin: center`
-   `perspective-origin: left`
-   `perspective-origin: right`
-   `perspective-origin: top`

## Values

\<length\>
:   A floating-point number, followed by either an absolute units designator (cm, mm, in, pt, or pc) or a relative units designator (em, ex, or px), that indicates the origin of transformation.

\<percentage\>
:   An integer, followed by a %. The value is a percentage of the total box length (for the first value) or the total box height (for the second value, if specified). The default is 50% 50%, as if the viewer was positioned directly in front of the object.

left
:   First value only. Equal to 0% or a zero length. This keyword displays the object as if the viewer were looking towards the left.

right
:   First value only. Equal to 100% or the full box length. This keyword displays the object as if the viewer were looking towards the right.

top
:   Second value only. Equal to 0% or a zero height. This keyword displays the object as if the viewer were looking towards the top.

bottom
:   Second value only. Equal to 100% or the full box height. This keyword displays the object as if the viewer were looking towards the bottom.

center
:   Equal to 50% or half the length of the box. When given as the first value, this keyword displays the object as if the viewer was positioned on par with the object, from left-to-right.

center
:   Equal to 50% or half the height of the box. When given as the second value, this keyword displays the object as if the viewer was positioned on par with the object, from top-to-bottom.

## Examples

In this example, the object class is a container, and the viewer class its child. SVG just creates the images. The perspective property must be used. And the transform property on the child gives it enough of an angle so the perspective-origin change is apparent. You can play around with the example by changing the perspective-origin values to the ones listed above. If you do, save your changes as a new gist, and add your example below!

``` css
.object {
    position: fixed;
    top: 100px;
    left: 0;
    right: 0;

    transform-style: preserve-3d;

    perspective: 1000px;
    perspective-origin: left;
}

.viewer {
    transform: rotateY(45deg);
}
```

[View live example](http://gist.github.com/7033692)

## Usage

     This property requires the perspective property. It has no effect on the child elements if the perspective property is not set for the object.

If only one value is specified, the second value is assumed to be *center*. If at least one of the two values is not a keyword, then the first value represents the horizontal position (or offset) and the second represents the vertical position (or offset).

## Notes

Perspective defines how an object is viewed. In graphic arts, perspective is the representation on a flat surface of what the viewer's eye would see in a 3D space. If there were a window between the viewer and the object, you could project points on the window surface that correspond to the points that exist beyond the glass. (See [Wikipedia](http://en.wikipedia.org/wiki/Perspective_(graphical)) for more information about graphical perspective and for related illustrations.)

The illusion of perspective on a flat surface, such as a computer screen, is created by projecting points on the flat surface as they would appear if the flat surface were a window through which the viewer was looking at the object. In discussion of virtual environments, this flat surface is called a projection plane. And the position of the viewer is towards some vanishing point. The perspective-origin sets the virtual gaze of the viewer towards some vanishing point.

## Related specifications

[CSS3 Transforms](http://www.w3.org/TR/css3-transforms/)
:   W3C Working Draft

## See also

### Other articles

-   [Manipulating content with CSS3 transforms - You need some perspective](/tutorials/css_transforms#You_need_some_perspective) by [Mike Sierra](/User:Sierra)

### External resources

-   [CSS 3D Transforms: Interactive Demo](http://sandbox.webpro.nl/css3/3d-transforms-interactive-demo.html) by [Lars Kappert](https://twitter.com/webprolific)
