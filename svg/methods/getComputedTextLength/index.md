---
title: getComputedTextLength
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'No editing form'
uri: svg/methods/getComputedTextLength

---
# getComputedTextLength

## Notes

### Remarks

The return value of the **getComputedTextLength** method enables Windows Internet Explorer to make reasonable assumptions about the glyph metrics for non-rendering processes.

The total text advance distance includes the advance values on the glyphs (horizontal or vertical), kerning effects, letter-spacing effects, word-spacing effects, and adjustments because of the [**dx**](/svg/properties/dx) and [**dy**](/svg/properties/dy) attributes on [**SVGTSpanElement**](/svg/elements/tspan) elements.

### Syntax

    float retVal = object.getComputedTextLength();

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## See also

### Related pages (MSDN)

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextContentElement**](/svg/elements/etextContent)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

