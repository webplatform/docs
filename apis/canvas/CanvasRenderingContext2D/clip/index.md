---
title: clip
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies a new clipping region by calculating the intersection of the current clipping region and the area described by the intended path, using the non-zero winding number rule. The new clipping region replaces the current clipping region.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/clip

---
## <span>Summary</span>

Specifies a new clipping region by calculating the intersection of the current clipping region and the area described by the intended path, using the non-zero winding number rule. The new clipping region replaces the current clipping region.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.clip();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example clips a region from a canvas, then draws a rectangle on the canvas, only part of which can be seen due to the clip.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
// Draw an open rectangle
ctxt.rect(50, 20, 200, 120);
ctxt.stroke();
// Clip the rectangle from the canvas
ctxt.clip();
// Draw filled rectangle in the upper left corner of the canvas after clip
ctxt.fillStyle = "green";
ctxt.fillRect(0, 0, 150, 100);
// Only the part of the filled rectangle that falls inside the clipped area is visible
</script>
```

## <span>Notes</span>

When the context is initialized, the clipping region must be set to the rectangle with the top left corner at (0,0) and the width and height at that of the coordinate space.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
