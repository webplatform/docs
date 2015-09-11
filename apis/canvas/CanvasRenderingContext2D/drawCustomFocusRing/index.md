---
title: drawCustomFocusRing
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Removed from spec; deletion candidate.'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: "Draw a focus ring of the appropriate style along the intended path, and sets result to false.\n"
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/drawCustomFocusRing

---
## <span>Summary</span>

Draw a focus ring of the appropriate style along the intended path, and sets result to false.

**Removed from spec; deletion candidate.**

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.drawCustomFocusRing(path, element);
```

## <span>Parameters</span>

### <span>path</span>

 Data-type
:   DOM Node

(Optional)

The path along which the focus ring is to be drawn.

### <span>element</span>

 Data-type
:   DOM Node

 The element on which the focus ring is to be drawn.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

**Needs Examples**: This section should include examples.

## <span>Notes</span>

The focus ring should not be subject to the shadow effects, the global alpha, or the global composition operators, but should be subject to the clipping region.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
