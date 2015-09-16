---
title: rotateFromVector
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/rotateFromVector

---
## Notes

### Remarks

The rotation angle is determined by taking (+/-)arctan(y/x). The direction of the vector (x,y) determines whether the positive or negative angle value is used. *Post-multiplies* means that other matrix operations are performed before this operation.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.3

## See also

### Related pages

-   [**SVGMatrix**](/svg/objects/SVGMatrix)
