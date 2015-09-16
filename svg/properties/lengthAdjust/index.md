---
title: lengthAdjust
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/lengthAdjust

---
## Notes

### Remarks

Indicates the type of adjustments to perform in order to make the rendered length of the text match the value specified on the [**textLength**](/svg/properties/textLength) attribute.

A value of **spacing** indicates that only the advance values are adjusted. The glyphs themselves are not stretched or compressed.

A value of **spacingAndGlyphs** indicates that the advance values are adjusted and the glyphs themselves are stretched or compressed in one axis (that is, in a direction parallel to the inline-progression direction).

The correct start and end positions for the text strings are guaranteed, but the locations of intermediate glyphs are not predictable because browsers might employ advanced algorithms to stretch or compress text strings in order to balance correct start and end positioning with optimal typography.

Be aware that, for a text string that contains *n* characters, the adjustments to the advance values often occur only for *n*-1 characters, whereas stretching or compressing of the glyphs will be applied to all *n* characters.

If the attribute is not specified, the effect is as if a value of **spacing** were specified.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.4

## See also

### Related pages (MSDN)

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextContentElement**](/svg/elements/etextContent)
