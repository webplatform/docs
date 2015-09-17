---
title: 'rotate()'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/10500f11ec6168049ba5'
compatibility:
  feature: rotate()
  topic: css
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].'
tags:
  - CSS_Functions
  - CSS
uri: css/functions/rotate()

---
## Summary

Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].

## Examples

The following code snippet is an example of the rotate function in use.

``` css
div {
  transform: rotate(33.3deg);
}
```

[View live example](http://gist.github.com/10500f11ec6168049ba5)

### Syntax

**rotate** `( <angle> )`

### Parameters

*angle*
:   The angle by which the element is rotated about its origin. If not specified otherwise, the element rotates around its center. The origin can be specified with the [transform-origin property](/css/properties/transform-origin). This value is expressed as an integer or decimal number followed by a supported angle unit.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.1

## Related specifications

[CSS Transforms Module Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145)
:   Working Draft

## See also

### Related pages

-   `Transform Functions`
-   Mathematical Description of Transform Functions[Mathematical Description of Transform Functions](http://go.microsoft.com/fwlink/p/?LinkId=256246)
-   Hands On: 2D Transforms[Hands On: 2D Transforms](http://go.microsoft.com/fwlink/?LinkID=240163)
