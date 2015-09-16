---
title: 'stroke'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: stroke
  topic: svg
notes:
  - 'Needs parent'
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
summary: 'The stroke attribute is a presentation attribute that define the color of the outline of the given graphical element.'
tags:
  - Markup
  - Attributes
  - SVG
uri: svg/attributes/stroke

---
## Summary

The stroke attribute is a presentation attribute that define the color of the outline of the given graphical element.

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
### Syntax

     stroke: none | currentColor | color | funciri [ none | currentColor | color ] | inherit

The default value is *none*, which means that the outline is not drawn.

## Examples

This example shows how to draw a circle with a red stroke and no fill color.

``` html


<svg width="400" height="400">
  <circle cx="100" cy="100" r="50" stroke="red" stroke-width="3" fill="none" />
</svg>
```

</pre>

### Standards information

-   [Scalable Vector Graphics: Painting, Filling, Stroking and Marker Symbols](http://www.w3.org/TR/SVG11/painting.html), Section 11.4

## Related specifications

[SVG 1.1](http://www.w3.org/TR/SVG11/painting.html#StrokeProperties)
:   W3C Recommendation

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

-   [**strokeDasharray**](/svg/attributes/stroke-dasharray)
-   [**strokeDashoffset**](/svg/attributes/stroke-dashoffset)
-   [**strokeLinecap**](/svg/attributes/stroke-linecap)
-   [**strokeLinejoin**](/svg/attributes/stroke-linejoin)
-   [**strokeMiterlimit**](/svg/attributes/stroke-miterlimit)
-   [**strokeOpacity**](/svg/attributes/stroke-opacity)
-   [**strokeWidth**](/svg/attributes/stroke-width)
-   [**fill**](/svg/attributes/fill)
