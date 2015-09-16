---
title: selectSubString
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/selectSubString

---
## Notes

### Remarks

The **selectSubString** method can raise a [**DOMException**](/dom/DOMException) excpetion with the code INDEX\_SIZE\_ERR. This exception is raised if the *charnum* or *nchars* parameter is negative or if *charnum* is greater than or equal to the number of characters at this node.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Text](http://go.microsoft.com/fwlink/p/?linkid=199818), Section 10.17.1

## See also

### Related pages

-   [**SVGTextElement**](/svg/elements/text)
-   [**SVGTextPositioningElement**](/svg/elements/textPositioning)
-   [**SVGTSpanElement**](/svg/elements/tspan)
-   [**SVGTextPathElement**](/svg/elements/textPath)
-   [**ISVGTextContentElement**](/svg/elements/etextContent)
