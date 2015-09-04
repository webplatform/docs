---
title: fillRect
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Paints the specified rectangular area using the color (or style) defined by fillStyle.'
uri: apis/canvas/CanvasRenderingContext2D/fillRect

---
# fillRect

## Summary

Paints the specified rectangular area using the color (or style) defined by fillStyle.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
 context.fillRect(x, y, width, height);
```

## Parameters

### x

 Data-typeÂ
:   Number

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### y

 Data-typeÂ
:   Number

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### width

 Data-typeÂ
:   Number

 The width, in pixels, of the rectangle in relation to the coordinates of the canvas. With value 0, the method has no effect.

### height

 Data-typeÂ
:   Number

 The height, in pixels, of the rectangle in relation to the coordinates of the canvas. With value 0, the method has no effect.

## Return Value

No return value

## Examples

This example sets a solid color fill style, then draws and fills a rectangle on the canvas.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "orange";
ctxt.fillRect(20, 20, 50, 120);
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

