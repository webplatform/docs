---
title: 'rx (SVGEllipseElement)'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: 'svg/properties/rx (SVGEllipseElement)'

---
## Examples

The following ellipse, centered within a 400 by 400 pixel square, has a major axis of 400 pixels (that is, 2 · **rx**) and a minor axis of 300 pixels (that is, 2 · [**ry**](/svg/properties/ry_(SVGEllipseElement))).

``` html


<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "http://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="400px" height="400px"
     viewBox="0 0 400 400" version="1.1" xmlns="http://www.w3.org/2000/svg">
  <desc>Major and Minor Axes of an SVG Ellipse</desc>
  <rect width="100%" height="100%" style="stroke: red; fill: none;"/>
  <ellipse cx="200" cy="200" rx="200" ry="150" style="fill: none; stroke: black;"/>
</svg>
```

</pre>

### Syntax

### Standards information

-   [Scalable Vector Graphics: Basic Shapes](http://go.microsoft.com/fwlink/p/?linkid=204737), Section 9.8.3

## See also

### Related pages

-   [**SVGEllipseElement**](/svg/elements/ellipse)
