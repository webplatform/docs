---
title: valueInSpecifiedUnits
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/valueInSpecifiedUnits

---
## Notes

### Remarks

If you set the **valueInSpecifiedUnits** property, the [**value**](/svg/properties/value) and [**valueAsString**](/svg/properties/valueAsString) properties are updated automatically to reflect this setting.

### Syntax

HRESULT value = object.put\_valueInSpecifiedUnits(float v);HRESULT value = object.get\_valueInSpecifiedUnits(float\* p);

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## See also

### Related pages (MSDN)

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
