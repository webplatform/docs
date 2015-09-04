---
title: getSubStringLength
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'No editing form'
uri: svg/methods/getSubStringLength

---
# getSubStringLength

## Notes

### Remarks

The total text advance distance includes the advance value on the glyphs (horizontal or vertical), kerning effects, letter-spacing effects, word-spacing effects, and adjustments because of the [**dx**](/svg/properties/dx) and [**dy**](/svg/properties/dy) attributes on [**tSpan**](/svg/elements/tspan) elements.

If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs, or because the range encompasses half of a surrogate pair), and if the *nchars* parameter is greater than 0, the measured range (i.e., total advance distance) is expanded so that each of the inseparable characters are included.

### Syntax

    float retVal = object.getSubStringLength(charnum, nchars);

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

