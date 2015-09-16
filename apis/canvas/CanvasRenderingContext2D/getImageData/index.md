---
title: 'getImageData'
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
summary: 'Returns an ImageData object representing the underlying pixel data for the area of the canvas denoted by the rectangle whose corners are the four points (sx, sy), (sx+sw, sy), (sx+sw, sy+sh), (sx, sy+sh), in canvas coordinate space units.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/getImageData

---
## Summary

Returns an ImageData object representing the underlying pixel data for the area of the canvas denoted by the rectangle whose corners are the four points (sx, sy), (sx+sw, sy), (sx+sw, sy+sh), (sx, sy+sh), in canvas coordinate space units.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.getImageData(sx, sy, sw, sh);
```

## Parameters

### sx

 Data-type
:   Number

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### sy

 Data-type
:   Number

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### sw

 Data-type
:   Number

 The width, in pixels, of the rectangle in relation to the coordinates of the canvas.

### sh

 Data-type
:   Number

 The height, in pixels, of the rectangle in relation to the coordinates of the canvas.

## Return Value

Returns an object of type DOM NodeDOM Node

**ICanvasImageData**

A *CanvasImageData* object with pixel information from the canvas within the specified coordinates.

## Examples

This example draws a solid color filled rectangle, then uses getImageData to retrieve part of the rectangle, and then uses putImageData to place that retrieved data elsewhere on the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "magenta";
ctxt.fillRect(10, 10, 75, 75);
var imgdata = ctxt.getImageData(10, 10, 30, 30);
ctxt.putImageData(imgdata, 100, 55);
</script>
```

## Notes

If the rectangle contains pixels outside the canvas, they are returned as transparent black. Pixels are returned as non-premultiplied alpha values.

## Related specifications

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
