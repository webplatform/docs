---
title: createLinearGradient
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a linear CanvasGradient initialized with the specified line as represented by the start point (x0, y0) and end point (x1, y1) of the gradient.'
uri: apis/canvas/CanvasRenderingContext2D/createLinearGradient

---
# createLinearGradient

## Summary

Returns a linear CanvasGradient initialized with the specified line as represented by the start point (x0, y0) and end point (x1, y1) of the gradient.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.createLinearGradient(x0, y0, x1, y1);
```

## Parameters

### x0

 Data-typeÂ
:   Number

 The x-coordinate, in pixels, of the start point of the gradient.

### y0

 Data-typeÂ
:   Number

 The y-coordinate, in pixels, of the start point of the gradient.

### x1

 Data-typeÂ
:   Number

 The x-coordinate, in pixels, of the end point of the gradient.

### y1

 Data-typeÂ
:   Number

 The y-coordinate, in pixels, of the end point of the gradient.

## Return Value

Returns an object of type DOM Node.

A **CanvasGradient** object that represents the new linear gradient.

## Examples

This example creates a diagonal (upper left to lower right) gradient, fading from red to yellow, and then places a rectangle filled with the gradient onto the canvas.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var grdt = ctxt.createLinearGradient(0, 0, 150, 150);
grdt.addColorStop(0, "red");
grdt.addColorStop(1, "yellow");
ctxt.fillStyle = grdt;
ctxt.fillRect(20, 20, 150, 100);
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

