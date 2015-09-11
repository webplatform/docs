---
title: getNumberOfChars
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - dom/properties/textContent
uri: svg/methods/getNumberOfChars

---
## <span>Notes</span>

### <span>Remarks</span>

The total number of characters includes referenced characters from **tref** reference, regardless of whether they are rendered.

The total number of characters is effectively equivalent to the length of the [**textContent**](/w/index.php?title=dom/properties/textContent&action=edit&redlink=1) attribute from the [DOM Level 3 Core](http://go.microsoft.com/fwlink/p/?linkid=203747) specification (section 1.4), if that attribute also expands **tref** elements.

### <span>Syntax</span>

     retVal = object.getNumberOfChars();

### <span>Standards information</span>

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**ISVGTextContentElement**](/svg/elements/etextContent)
