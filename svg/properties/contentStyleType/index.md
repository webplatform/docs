---
title: 'contentStyleType'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/contentStyleType

---
## Notes

### Remarks

Do not set the **contentStyleType** property. If you try to set this property, it causes an error.

Because CSS is the only common language for inline styling, and because CSS is the default language if you do not specify the **contentStyleType** property, all browsers do not support this property well. As a result, the **contentStyleType** property and its corresponding attribute are deprecated. You should not use this property in new content. Future versions of the SVG specification might remove this property.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.2

## See also

### Related pages

-   [**SVGSVGElement**](/svg/elements/svg)
