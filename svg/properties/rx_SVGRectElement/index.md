---
title: rx (SVGRectElement)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: 'svg/properties/rx (SVGRectElement)'

---
## Notes

### Remarks

If you properly specify a value for the **rx** property but not for the [**ry**](/svg/properties/ry_(SVGRectElement)) property, the [**rect**](/svg/elements/rect) element is rendered with the effective value of **ry** equal to **rx**. If you properly specify a value for **ry** but not for **rx**, the **rect** element is rendered with the effective value of **rx** equal to **ry**.

If you do not property specify **rx** or [**ry**](/svg/properties/ry_(SVGRectElement)) , the [**rect**](/svg/elements/rect) element is rendered without rounding, resulting in square corners.

If **rx** is greater than half of the width of the rectangle, the [**rect**](/svg/elements/rect) element is rendered with the effective value for **rx** as half of the width of the rectangle. If [**ry**](/svg/properties/ry_(SVGRectElement)) is greater than half of the height of the rectangle, the **rect** element is rendered with the effective value for **ry** as half of the height of the rectangle.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Basic Shapes](http://go.microsoft.com/fwlink/p/?linkid=204737), Section 9.8.1

## See also

### Related pages

-   [**SVGRectElement**](/svg/elements/rect)
-   [**ellipse**](/svg/elements/ellipse)
