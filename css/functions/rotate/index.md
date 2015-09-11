---
title: rotate()
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
code_samples:
  - 'http://gist.github.com/10500f11ec6168049ba5'
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].'
tags:
  - CSS
  - Functions
uri: css/functions/rotate()

---
## <span>Summary</span>

Rotates an element clockwise around its origin (as specified by the transform-origin property) by the specified angle. The operation corresponds to the matrix [cos(angle) sin(angle) -sin(angle) cos(angle) 0 0].

## <span>Examples</span>

The following code snippet is an example of the rotate function in use.

``` css
div {
  transform: rotate(33.3deg);
}
```

[View live example](http://code.webplatform.org/gist/10500f11ec6168049ba5)

### <span>Syntax</span>

**rotate** `( <angle> )`

### <span>Parameters</span>

*angle*
:   The angle by which the element is rotated about its origin. If not specified otherwise, the element rotates around its center. The origin can be specified with the [transform-origin property](http://docs.webplatform.org/wiki/css/properties/transform-origin). This value is expressed as an integer or decimal number followed by a supported angle unit.

### <span>Standards information</span>

-   [CSS Transforms Module, Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145), Section 13.1

## <span>Related specifications</span>

[CSS Transforms Module Level 3](http://go.microsoft.com/fwlink/p/?LinkID=223145)
:   Working Draft

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Transform Functions`
-   `Mathematical Description of Transform Functions`
-   `Hands On: 2D Transforms`
