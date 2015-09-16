---
title: pathSegList
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Unreviewed MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/properties/pathSegList

---
## Notes

### Remarks

With the **pathSegList** property, you can access the base (or *static*) contents of the [**d**](/svg/properties/d) attribute in a form that directly matches the SVG syntax. If the **d** attribute contains an "absolute moveto (M)" and an "absolute arcto (A)" command, **pathSegList** contains two entries: SVG\_PATHSEG\_MOVETO\_ABS and SVG\_PATHSEG\_ARC\_ABS.

### Syntax

### Standards information

-   [Scalable Vector Graphics: Paths](http://go.microsoft.com/fwlink/p/?linkid=204736), Section 8.5.22

## See also

### Related pages (MSDN)

-   [**SVGPathElement**](/svg/elements/path)
-   [**animatedPathSegList**](/svg/properties/animatedPathSegList)
