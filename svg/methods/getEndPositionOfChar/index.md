---
title: getEndPositionOfChar
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'No editing form'
uri: svg/methods/getEndPositionOfChar

---
# getEndPositionOfChar

## Notes

### Remarks

The character's current text position does not consider the effects of any inter-character adjustments to prepare for the next character, such as kerning, letter spacing, word spacing, and adjustments because of the [**x**](/svg/properties/x), [**y**](/svg/properties/y), [**dx**](/svg/properties/dx), and [**dy**](/svg/properties/dy) attributes. If multiple consecutive characters are rendered inseparably (for example, as a single glyph or a sequence of glyphs), each of the inseparable characters returns the end position for the last glyph.

### Syntax

    ISVGPoint retVal = object.getEndPositionOfChar(charnum);

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

