---
title: 'gradientUnits'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/gradientUnits

---
## Notes

### Remarks

When *p* is **objectBoundingBox** and the [**gradientTransform**](/svg/properties/gradientTransform) property is the identity matrix, the normal of the linear gradient is perpendicular to the gradient vector in object bounding box space. When the object's bounding box is not square, the gradient normal (which is initially perpendicular to the gradient vector within object bounding box space) might render non-perpendicular relative to the gradient vector in user space. If the gradient vector is parallel to one of the axes of the bounding box, the gradient normal remains perpendicular. This transformation occurs because of the non-uniform scaling transformation from bounding box space to user space.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.1

## See also

### Related pages

-   [**SVGGradientElement**](/svg/elements/gradient)
-   [**SVGLinearGradientElement**](/svg/elements/linearGradient)
-   [**SVGRadialGradientElement**](/svg/elements/radialGradient)
