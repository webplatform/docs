---
title: rotate()
tags:
  - CSS
  - Functions
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].'
code_samples:
  - 'http://gist.github.com/10500f11ec6168049ba5'
uri: css/functions/rotate()

---
# rotate()

## Summary

Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].

## Examples

The following code snippet is an example of the rotate function in use.

``` {.css}
div {
  transform: rotate(33.3deg);
}
```

[View live example](http://code.webplatform.org/gist/10500f11ec6168049ba5)

### Syntax

**rotate** `( <angle> )`

### Parameters

*angle*
:   The angle by which the element is rotated about its origin. If not specified otherwise, the element rotates around its center. The origin can be specified with the [transform-origin property](http://docs.webplatform.org/wiki/css/properties/transform-origin). This value is expressed as an integer or decimal number followed by a supported angle unit.

### Standards information

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.1

## Related specifications

Specification
:   Status
[CSS Transforms Module Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145)
:   Working Draft

## See also

### Related pages (MSDN)

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Hands On: 2D Transforms`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

