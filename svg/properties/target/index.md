---
title: 'target'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/target

---
## Examples

The following code example shows the default and **\_blank** behaviors of the **target** property.

``` html


<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN"
 "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="5cm" height="7cm" viewBox="0 0 5 7" version="1.1" xmlns="http://www.w3.org/2000/svg"
     xmlns:xlink="http://www.w3.org/1999/xlink">
  <desc>Two basic link types.</desc>
  <!-- Outline the SVG viewport. -->
  <rect x="0" y="0" width="100%" height="100%" fill="none" stroke="blue"  stroke-width=".03"/>
  <a xlink:href="http://www.w3.org">
    <ellipse cx="2.5" cy="1.5" rx="2" ry="1" fill="red" />
  </a>
  <a xlink:href="http://dev.w3.org/SVG/profiles/1.1F2/publish/" target="_blank">
    <ellipse cx="2.5" cy="4.75" rx="2" ry="1" fill="green" />
  </a>
</svg>
```

</pre>

## Notes

### Remarks

The **target** property specifies the name or portion of the target window, frame, pane, tab, or other relevant presentation context (that is, an HTML or XHTML frame, iframe, or object element) where a document is opened when the link is activated.

Use **target** when there are multiple possible targets for the ending resource, such as when the parent document is a multi-frame HTML or XHTML document.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Linking](http://go.microsoft.com/fwlink/p/?linkid=199815), Section 17.2

## See also

### Related pages

-   [**SVGAElement**](/svg/elements/a)
