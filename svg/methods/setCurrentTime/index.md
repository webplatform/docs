---
title: setCurrentTime
tags:
  - SVG
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'No editing form'
uri: svg/methods/setCurrentTime

---
# setCurrentTime

## Notes

### Remarks

If you call the **setCurrentTime** method before the document timeline has begun (for example, by a script that is running in a [**script**](/svg/elements/script) element before the [**SVGLoad**](/svg/events/load) event for the document is dispatched), the value of *seconds* during the last call to **setCurrentTime** is the current time.

### Syntax

    var retval = SVGSVGElement.setCurrentTime(seconds);

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.2

## See also

### Related pages (MSDN)

-   [**SVGSVGElement**](/svg/elements/svg)

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

