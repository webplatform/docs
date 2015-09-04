---
title: moveTo
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Creates a new subpath with the specified point as its first (and only) point.'
uri: apis/canvas/CanvasRenderingContext2D/moveTo

---
# moveTo

## Summary

Creates a new subpath with the specified point as its first (and only) point.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.moveTo(x, y);
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

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

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

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

