---
title: fx
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/fx

---
## Notes

### Remarks

The **fx** and [**fy**](/svg/properties/fy) properties define the focal point for the radial gradient. The gradient is drawn such that the 0% gradient stop is mapped to the point (fx, fy). If you do not specify the **fx** attribute, **fx** coincides with the presentational value of [**cx**](/svg/properties/cx_(SVGRadialGradientElement)) for the element, whether the value for **cx** is inherited or not. If the element references an element that specifies a value for **fx**, the value of **fx** is inherited from the referenced element. You can animate the **fx** property.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.3

## See also

### Related pages

-   [**SVGRadialGradientElement**](/svg/elements/radialGradient)

### Reference

-   [**fy**](/svg/properties/fy)
-   [**r**](/svg/properties/r_(SVGRadialGradientElement))
