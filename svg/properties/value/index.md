---
title: value
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'Unreviewed MSDN import'
uri: svg/properties/value

---
# value

## Notes

### Remarks

For angles, the **value** property is in degrees. For lengths, the **value** property is in user units. If you

set the **value** property, the [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits) and [**valueAsString**](/svg/properties/valueAsString) properties are updated automatically to reflect this setting.

### Syntax

HRESULT value = object.put\_value(float v);HRESULT value = object.get\_value(float\* p);

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## See also

### Related pages (MSDN)

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
-   [**SVGNumber**](/svg/objects/SVGNumber)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

