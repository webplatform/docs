---
title: setCurrentTime
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'No editing form'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/setCurrentTime

---
## Notes

### Remarks

If you call the **setCurrentTime** method before the document timeline has begun (for example, by a script that is running in a [**script**](/svg/elements/script) element before the [**SVGLoad**](/svg/events/load) event for the document is dispatched), the value of *seconds* during the last call to **setCurrentTime** is the current time.

### Syntax

    var retval = SVGSVGElement.setCurrentTime(seconds);

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.2

## See also

### Related pages

-   [**SVGSVGElement**](/svg/elements/svg)
