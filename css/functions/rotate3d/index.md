---
title: rotate3d()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
summary: 'Defines a three-dimensional rotation transformation by first defining the axis of rotation as an (x,y,z) vector and then defining the angle to rotate the element around this axis.  Requires four parameters: the first three are unitless numbers defining the axis vector, and the fourth is an angle measurement (specifying degrees or radians).'
code_samples:
  - 'http://gist.github.com/5304145'
uri: css/functions/rotate3d()

---
# rotate3d()

## Summary

Defines a three-dimensional rotation transformation by first defining the axis of rotation as an (x,y,z) vector and then defining the angle to rotate the element around this axis. Requires four parameters: the first three are unitless numbers defining the axis vector, and the fourth is an angle measurement (specifying degrees or radians).

## Examples

The following code snippet is an example of the **rotate3d** function in use. When applied to a square blue [**div**](/html/elements/div) element, it has the effect illustrated in the image. (The light-blue square indicates the original position of the transformed element.)

``` {.css}
div {
   transform: rotate3d(0.7, 0.5, 0.7, 45deg);
}
```

[View live example](http://code.webplatform.org/gist/5304145)

## Notes

### Remarks

The element rotates by the angle specified in the last parameter, and about the [*x*,*y*,*z*] direction vector described by the first three parameters. If the direction vector is not of unit length, it will be normalized. A direction vector that cannot be normalized, such as [0, 0, 0], results in no rotation.

### Syntax

**rotate3d** `( <number>  ,  <number>  ,  <number>  ,  <angle> )`

### Parameters

*number*
:   A component of the direction vector about which the element is rotated.
*angle*
:   The angle by which the element is rotated. This value is expressed as a number followed by a supported angle unit.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.2

## See also

### Related articles

#### Transforms

-   [inverse](/css/cssom/MSCSSMatrix/methods/inverse)

-   [multiply](/css/cssom/MSCSSMatrix/methods/multiply)

-   [rotate](/css/cssom/MSCSSMatrix/methods/rotate)

-   **rotate3d()**

-   [scale3d()](/css/functions/scale3d())

-   [skew()](/css/functions/skew())

-   [translate()](/css/functions/translate())

-   [translate3d()](/css/functions/translate3d())

-   [translateX()](/css/functions/translateX())

-   [translateY()](/css/functions/translateY())

-   [translateZ()](/css/functions/translateZ())

-   [backface-visibility](/css/properties/backface-visibility)

-   [transform-origin-z](/css/properties/transform-origin-z)

-   [MSCSSMatrix](/css/transforms/MSCSSMatrix)

-   [translate](/css/transforms/MSCSSMatrix/translate)

-   [JavaScript animation](/tutorials/animation_in_javascript_2)

### Related pages (MSDN)

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Direct3D: Matrices`
-   `Hands On: 3-D Transforms`

### Related pages (HTML5Rocks)

-   `3D and CSS`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/3d/css/)

