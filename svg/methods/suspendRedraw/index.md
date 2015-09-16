---
title: suspendRedraw
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Stub MSDN import'
readiness: 'Not Ready'
standardization_status: Unknown
tags:
  - SVG
uri: svg/methods/suspendRedraw

---
## Notes

### Remarks

The redrawing operation is suspended until one of the following actions occur:

-   The [**unsuspendRedraw**](/svg/methods/unsuspendRedraw) method is called.
-   The [**unsuspendRedrawAll**](/svg/methods/unsuspendRedrawAll) method is called.
-   The *maxWaitMilliseconds* time-out interval elapses.

### Syntax

    var retval = SVGSVGElement.suspendRedraw(maxWaitMilliseconds);

### Standards information

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.2

## See also

### Related pages (MSDN)

-   [**SVGSVGElement**](/svg/elements/svg)
