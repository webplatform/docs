---
title: convertToSpecifiedUnits
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/convertToSpecifiedUnits

---
## <span>Notes</span>

### <span>Remarks</span>

The **convertToSpecifiedUnits** method preserves the same underlying stored value, but it resets the stored unit identifier to the specified *unitType* type. The [**unitType**](/svg/properties/unitType_(SVGLength)), [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits), and [**valueAsString**](/svg/properties/valueAsString) objects might be modified when you call this method.

### <span>Syntax</span>

    HRESULT retVal = object.convertToSpecifiedUnits(unitType);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
