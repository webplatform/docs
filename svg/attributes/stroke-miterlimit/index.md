---
title: 'stroke-miterlimit'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: stroke-miterlimit
  topic: svg
notes:
  - 'Needs all content'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/attributes/stroke-miterlimit

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Notes

### Remarks

The ratio of miter length (distance between the outer tip and the inner corner of the miter) to [**strokeWidth**](/svg/attributes/stroke-width) is directly related to the angle (theta) between the segments in user space by the formula: **miterLength / stroke-width = 1 / sin ( theta / 2 )**

### Syntax

    stroke-miterlimit: inherit

### Standards information

-   [Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols](http://go.microsoft.com/fwlink/p/?linkid=199816), Section 11.4

## See also

### Related pages

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
-   [**currentStyle**](/css/cssom/currentStyle)
-   [**style**](/css/cssom/style)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGPathElement**](/svg/elements/path)
-   [**SVGRectElement**](/svg/elements/rect)
-   [**SVGCircleElement**](/svg/elements/circle)
-   [**SVGEllipseElement**](/svg/elements/ellipse)
-   [**SVGLineElement**](/svg/elements/line)
-   [**SVGPolylineElement**](/svg/elements/polyline)
-   [**SVGPolygonElement**](/svg/elements/polygon)

### Reference

-   [**stroke**](/svg/attributes/stroke)
-   [**strokeDasharray**](/svg/attributes/stroke-dasharray)
-   [**strokeDashoffset**](/svg/attributes/stroke-dashoffset)
-   [**strokeLinecap**](/svg/attributes/stroke-linecap)
-   [**strokeLinejoin**](/svg/attributes/stroke-linejoin)
-   [**strokeOpacity**](/svg/attributes/stroke-opacity)
-   [**strokeWidth**](/svg/attributes/stroke-width)
