---
title: closePath
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Marks the last subpath as closed, creates a new subpath whose first point is the same as the previous subpath''s last point, and then adds the new subpath to the path, returning to the first subpath''s first point (closing the shape). If the object''s path has no subpaths, this method does nothing.'
uri: apis/canvas/CanvasRenderingContext2D/closePath

---
# closePath

## Summary

Marks the last subpath as closed, creates a new subpath whose first point is the same as the previous subpath's last point, and then adds the new subpath to the path, returning to the first subpath's first point (closing the shape). If the object's path has no subpaths, this method does nothing.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.closePath();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example draws two lines at right angles, then uses closePath to connect the start and end points.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
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

## Notes

If the last subpath has more than one point in its list of points, then this is equivalent to adding a straight line connecting the last point back to the first point, thus closing the shape, and then repeating the last (possibly implied) *moveTo()* call.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

