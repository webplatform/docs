---
title: closePath
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
summary: 'Marks the last subpath as closed, creates a new subpath whose first point is the same as the previous subpath''s last point, and then adds the new subpath to the path, returning to the first subpath''s first point (closing the shape). If the object''s path has no subpaths, this method does nothing.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/closePath

---
## <span>Summary</span>

Marks the last subpath as closed, creates a new subpath whose first point is the same as the previous subpath's last point, and then adds the new subpath to the path, returning to the first subpath's first point (closing the shape). If the object's path has no subpaths, this method does nothing.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.closePath();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This example draws two lines at right angles, then uses closePath to connect the start and end points.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.beginPath();
ctxt.moveTo(10,10);
ctxt.lineTo(10,100);
ctxt.lineTo(50,100);
ctxt.closePath();
ctxt.stroke();
</script>
```

## <span>Notes</span>

If the last subpath has more than one point in its list of points, then this is equivalent to adding a straight line connecting the last point back to the first point, thus closing the shape, and then repeating the last (possibly implied) *moveTo()* call.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
