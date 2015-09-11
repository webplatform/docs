---
title: getComputedTextLength
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/getComputedTextLength

---
## <span>Notes</span>

### <span>Remarks</span>

The return value of the **getComputedTextLength** method enables Windows Internet Explorer to make reasonable assumptions about the glyph metrics for non-rendering processes.

The total text advance distance includes the advance values on the glyphs (horizontal or vertical), kerning effects, letter-spacing effects, word-spacing effects, and adjustments because of the [**dx**](/svg/properties/dx) and [**dy**](/svg/properties/dy) attributes on [**SVGTSpanElement**](/svg/elements/tspan) elements.

### <span>Syntax</span>

    float retVal = object.getComputedTextLength();

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextContentElement**](/svg/elements/etextContent)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
