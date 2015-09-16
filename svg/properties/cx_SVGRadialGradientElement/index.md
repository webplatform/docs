---
title: cx (SVGRadialGradientElement)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: 'svg/properties/cx (SVGRadialGradientElement)'

---
## Notes

### Remarks

The **cx** property defines the x-coordinate for the center of the largest (that is, outermost) circle of a radial gradient. The gradient is drawn such that the 100% gradient [**stop**](/svg/elements/stop) is mapped to the perimeter of this largest (that is, outermost) circle. If you do not specify the **cx** property, the effect is the same as if you specify a value of **50%**.

The **cx** value can be a percentage. When [**gradientUnits**](/svg/properties/gradientUnits) is **userSpaceOnUse**, percentages represent values that are relative to the current viewport. When **gradientUnits** is **objectBoundingBox**, percentages represent values that are relative to the bounding box for the object.

Properties inherit into the [**radialGradient**](/svg/elements/radialGradient) element from its ancestors. Properties do not inherit from the element that references the **radialGradient** element.

[**radialGradient**](/svg/elements/radialGradient) elements are never rendered directly. They exist so that you can reference them by using the **fill** and **stroke** properties.

The **display** property does not apply to the [**radialGradient**](/svg/elements/radialGradient) element so **radialGradient** elements are not directly rendered even if the **display** property is set to a value other than **none**. **radialGradient** elements are available for referencing even when the **display** property on the **radialGradient** element or any of its ancestors is set to **none**.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Gradients and Patterns](http://go.microsoft.com/fwlink/p/?linkid=199811), Section 13.4.3

## See also

### Related pages

-   [**SVGRadialGradientElement**](/svg/elements/radialGradient)
