---
title: 'strokeRect'
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
summary: 'Takes the result of tracing the path, using the CanvasRenderingContext2D object''s line styles, and fills it with the strokeStyle.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/strokeRect

---
## Summary

Takes the result of tracing the path, using the CanvasRenderingContext2D object's line styles, and fills it with the strokeStyle.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.strokeRect(x, y, w, h);
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

### w

 Data-type
:   Number

 The width, in pixels, of the rectangle in relation to the coordinates of the canvas.

### h

 Data-type
:   Number

 The height, in pixels, of the rectangle in relation to the coordinates of the canvas.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

Basic example drawing a 100 x 100 px rect with a red outline

``` js
// draw rect with red outline
ctx.strokeStyle = 'red';
ctx.strokeRect(10,10,100,100);
```

Draws a rect with a white outline onto a black canvas

``` html
<!DOCTYPE html>
<html>
<head>
  <title>Canvas Example</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d");

        // clear background
        ctx.fillStyle = 'black';
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        // draw rect with outline
        ctx.strokeStyle = 'white';
        ctx.strokeRect(10,10,100,100);

      }
    }
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

## Notes

The *strokeRect* method creates a path that requires the use of the [stroke](/apis/canvas/CanvasRenderingContext2D/stroke) method to render the rectangle. The outline uses the current [strokeStyle](/apis/canvas/CanvasRenderingContext2D/strokeStyle), [lineWidth](/apis/canvas/CanvasRenderingContext2D/lineWidth), [lineJoin](/apis/canvas/CanvasRenderingContext2D/lineJoin), and, when appropriate, [miterLimit](/apis/canvas/CanvasRenderingContext2D/miterLimit) properties. If the *w* or *h* parameter is zero, a line is drawn. If the *w* and *h* parameters are zero, the rectangle is not drawn.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
