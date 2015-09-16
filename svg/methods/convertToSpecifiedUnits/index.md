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
## Notes

### Remarks

The **convertToSpecifiedUnits** method preserves the same underlying stored value, but it resets the stored unit identifier to the specified *unitType* type. The [**unitType**](/svg/properties/unitType_(SVGLength)), [**valueInSpecifiedUnits**](/svg/properties/valueInSpecifiedUnits), and [**valueAsString**](/svg/properties/valueAsString) objects might be modified when you call this method.

### Syntax

    HRESULT retVal = object.convertToSpecifiedUnits(unitType);

### Standards information

-   [Scalable Vector Graphics: Basic Data Types and Interfaces](http://go.microsoft.com/fwlink/p/?linkid=204732), Section 4.5.11

## See also

### Related pages

-   [**SVGAngle**](/svg/objects/SVGAngle)
-   [**SVGLength**](/svg/objects/SVGLength)
