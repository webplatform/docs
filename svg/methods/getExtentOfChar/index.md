---
title: getExtentOfChar
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/getExtentOfChar

---
## <span>Notes</span>

### <span>Remarks</span>

The calculations for the rectangle assume that all glyphs occupy the full standard glyph cell for the font. If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs), each of the inseparable characters returns the same rectangle.

### <span>Syntax</span>

    ISVGRect retVal = object.getExtentOfChar(charnum);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**SVGTextContentElement**](/svg/elements/etextContent)
