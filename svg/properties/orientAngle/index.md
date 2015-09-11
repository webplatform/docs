---
title: orientAngle
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/orientAngle

---
## <span>Notes</span>

### <span>Remarks</span>

If the [**orientType**](/svg/properties/orientType) property is **SVG\_MARKER\_ORIENT\_ANGLE**, this property represents the angle value for **orientAngle**; otherwise, this property is set to zero.

### <span>Syntax</span>

HRESULT value = object.put\_orientAngle(ISVGAnimatedAngle\* v);HRESULT value = object.get\_orientAngle(ISVGAnimatedAngle\*\* p);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols](http://go.microsoft.com/fwlink/p/?linkid=199816), Section 11.9.2

## <span>See also</span>

### <span>Related pages (MSDN)</span>

### <span>Reference</span>

-   [**SVGMarkerElement**](/svg/elements/marker)
-   [**orientType**](/svg/properties/orientType)
