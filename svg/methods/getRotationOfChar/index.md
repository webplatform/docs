---
title: getRotationOfChar
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/getRotationOfChar

---
## Notes

### Remarks

If multiple glyphs are used to render the specified character and if the glyphs each have different rotations (for example, because of text-on-a-path), the **getRotationOfChar** method returns an average value (that is, the rotation angle at the midpoint along the path for all glyphs that are used to render the specified character).

The rotation value represents the rotation that is supplemental to any rotation because of the [**glyphOrientationHorizontal**](/svg/attributes/glyph-orientation-horizontal) and [**glyphOrientationVertical**](/svg/attributes/glyph-orientation-vertical) properties. Any glyph rotations because of these properties are not included in the returned rotation value.

If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs), each of the inseparable characters returns the same rotation value.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## See also

### Related pages

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextContentElement**](/svg/elements/etextContent)
