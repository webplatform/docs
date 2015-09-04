---
title: lineTo
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Connects the last point in the subpath to the given point (x, y) using a straight line, and then adds the point to the subpath.'
uri: apis/canvas/CanvasRenderingContext2D/lineTo

---
# lineTo

## Summary

Connects the last point in the subpath to the given point (x, y) using a straight line, and then adds the point to the subpath.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
 context.lineTo(x, y);
```

## Parameters

### x

 Data-typeÂ
:   Number

 The x-coordinate, in pixels.

### y

 Data-typeÂ
:   Number

 The y-coordinate, in pixels.

## Return Value

No return value

## Examples

This example uses moveTo to establish a subpath starting point, and then uses lineTo to add line segments.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.beginPath();
ctxt.moveTo(50,75);
ctxt.lineTo(150, 75);
ctxt.lineTo(200, 125);
ctxt.stroke();
</script>
```

## Notes

If subpath is not allocated, the user agent will create it. If subpath has no any point (x, y), then point (x, y) will be created for subpath as its first (and only) point, as if the *moveTo(x, y)* method had been called.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

