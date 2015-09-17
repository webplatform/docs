---
title: 'enable-background'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
compatibility:
  feature: enable-background
  topic: svg
notes:
  - 'Needs all content'
readiness: 'Not Ready'
tags:
  - Markup_Attributes
  - SVG
  - Needs_Summary
  - Needs_Examples
uri: svg/attributes/enable-background

---
<table class="wikitable">
<tr>
<th>
Applies to

</th>
<td>
 ?

</td>
</tr>
</table>
## Notes

### Remarks

The optional *x*, *y*, *width*, *height* parameters on the new value are numeric values that indicate the subregion of the container element's user space where access to the background image is allowed to happen. These parameters enable the SVG user agent potentially to allocate smaller temporary image buffers than the default values.

### Syntax

    enable-background: accumulate |' new [ x y width height ]'? | inherit

### Standards information

-   [Scalable Vector Graphics: Filter Effects](http://go.microsoft.com/fwlink/p/?linkid=226062), Section 15.6

## See also

### Related pages

-   [**CSSStyleDeclaration**](/css/cssom/CSSStyleDeclaration/CSSStyleDeclaration)
