---
title: 'fillRect'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Paints the specified rectangular area using the color (or style) defined by fillStyle.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/fillRect

---
## Summary

Paints the specified rectangular area using the color (or style) defined by fillStyle.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 context.fillRect(x, y, width, height);
```

## Parameters

### x

 Data-type
:   Number

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### y

 Data-type
:   Number

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### width

 Data-type
:   Number

 The width, in pixels, of the rectangle in relation to the coordinates of the canvas. With value 0, the method has no effect.

### height

 Data-type
:   Number

 The height, in pixels, of the rectangle in relation to the coordinates of the canvas. With value 0, the method has no effect.

## Return Value

No return value

## Examples

This example sets a solid color fill style, then draws and fills a rectangle on the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "orange";
ctxt.fillRect(20, 20, 50, 120);
</script>
```

## Related specifications

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
