---
title: value
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/value

---
## <span>Notes</span>

### <span>Remarks</span>

For angles, the **value** property is in degrees. For lengths, the **value** property is in user units. If you

set the **value** property, the [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits) and [**valueAsString**](/svg/properties/valueAsString) properties are updated automatically to reflect this setting.

### <span>Syntax</span>

HRESULT value = object.put\_value(float v);HRESULT value = object.get\_value(float\* p);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
-   [**SVGNumber**](/svg/objects/SVGNumber)
