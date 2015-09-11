---
title: valueAsString
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/valueAsString

---
## <span>Notes</span>

### <span>Remarks</span>

If you set the **valueAsString** property, the [**value**](/svg/properties/value), [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits), and **svgUnitTypes** properties are updated automatically to reflect this setting.

### <span>Syntax</span>

HRESULT value = object.put\_valueAsString(BSTR v);HRESULT value = object.get\_valueAsString(BSTR\* p);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
