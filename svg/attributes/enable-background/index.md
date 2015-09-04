---
title: enable-background
tags:
  - Markup
  - Attributes
  - SVG
readiness: 'Not Ready'
notes:
  - 'Needs all content'
uri: svg/attributes/enable-background

---
# enable-background

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Applies to
:    ?

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The optional *x*, *y*, *width*, *height* parameters on the new value are numeric values that indicate the subregion of the container element's user space where access to the background image is allowed to happen. These parameters enable the SVG user agent potentially to allocate smaller temporary image buffers than the default values.

### Syntax

    enable-background: accumulate |' new [ x y width height ]'? | inherit

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.6

## See also

### Related pages (MSDN)

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

