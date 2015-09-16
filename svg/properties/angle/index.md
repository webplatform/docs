---
title: 'angle'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/angle

---
## Notes

### Remarks

For angle values in properties and their corresponding presentation attributes, the angle unit identifier is optional. If you do not the identifier, the angle value is treated as if it is in degrees. If you provide the identifier, the angle unit identifier must be in lowercase.

When you use angles in an SVG attribute, the **angle** property is defined as **deg** for degrees, **grad** for gradians, or **rad** for radians. In the SVG DOM, **angle** values are represented by using [**SVGAngle**](/svg/objects/SVGAngle) or [**SVGAnimatedAngle**](/svg/objects/SVGAnimatedAngle) objects.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.1

## See also

### Related pages

-   [**SVGPathSegArcAbs**](/svg/objects/SVGPathSegArcAbs)
-   [**SVGPathSegArcRel**](/svg/objects/SVGPathSegArcRel)
-   [**SVGTransform**](/svg/objects/SVGTransform)
