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
## <span>Notes</span>

### <span>Remarks</span>

The redrawing operation is suspended until one of the following actions occur:

-   The [**unsuspendRedraw**](/svg/methods/unsuspendRedraw) method is called.
-   The [**unsuspendRedrawAll**](/svg/methods/unsuspendRedrawAll) method is called.
-   The *maxWaitMilliseconds* time-out interval elapses.

### <span>Syntax</span>

    var retval = SVGSVGElement.suspendRedraw(maxWaitMilliseconds);

### <span>Standards information</span>

-   [Scalable Vector Graphics: Document Structure](http://go.microsoft.com/fwlink/p/?linkid=204733), Section 5.11.2

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   [**SVGSVGElement**](/svg/elements/svg)
