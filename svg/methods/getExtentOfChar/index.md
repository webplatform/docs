---
title: getExtentOfChar
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'No editing form'
uri: svg/methods/getExtentOfChar

---
# getExtentOfChar

## Notes

### Remarks

The calculations for the rectangle assume that all glyphs occupy the full standard glyph cell for the font. If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs), each of the inseparable characters returns the same rectangle.

### Syntax

    ISVGRect retVal = object.getExtentOfChar(charnum);

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## See also

### Related pages (MSDN)

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextContentElement**](/svg/elements/etextContent)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

