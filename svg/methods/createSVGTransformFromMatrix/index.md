---
title: createSVGTransformFromMatrix
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/createSVGTransformFromMatrix

---
## Notes

### Remarks

The **createSVGTransformFromMatrix** method creates an [**SVGTransform**](/svg/objects/SVGTransform) object, of transform type SVG\_TRANSFORM\_MATRIX, whose values are given by the *matrix* parameter. The values from the *matrix* parameter are copied; the *matrix* parameter is not adopted as the [**matrix**](/svg/properties/matrix) property.

The [**SVGTransform**](/svg/objects/SVGTransform) object corresponds to a single **matrix()** component within an element's **transform** attribute specification.

**Note:** For [**SVGSVGElement**](/svg/elements/svg) elements, the [**SVGTransform**](/svg/objects/SVGTransform) object is created outside of any document trees.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Coordinate Systems, Transformations and Units](http://go.microsoft.com/fwlink/p/?linkid=204735), Section 7.14.5

## See also

### Related pages (MSDN)

-   [**SVGSVGElement**](/svg/elements/svg)
-   [**SVGTransformList**](/svg/objects/SVGTransformList)
-   [**SVGMatrix**](/svg/objects/SVGMatrix)
