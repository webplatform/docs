---
title: drawSystemFocusRing
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Removed from spec; deletion candidate.'
summary: "Draws a focus ring of the appropriate style along the intended path, following platform conventions.\n"
uri: apis/canvas/CanvasRenderingContext2D/drawSystemFocusRing

---
# drawSystemFocusRing

## Summary

Draws a focus ring of the appropriate style along the intended path, following platform conventions.

**Removed from spec; deletion candidate.**

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.drawSystemFocusRing(path, element);
```

## Parameters

### path

 Data-typeÂ
:   DOM Node

*(Optional)*

The path along which the focus ring is to be drawn.

### element

 Data-typeÂ
:   DOM Node

 The element on which the focus ring is to be drawn.

## Return Value

Returns an object of type DOM Node.

**Needs Examples**: This section should include examples.

## Notes

The focus ring should not be subject to the shadow effects, the global alpha, or the global composition operators, but should be subject to the clipping region.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

