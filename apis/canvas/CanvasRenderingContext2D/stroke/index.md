---
title: 'stroke'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Traces the intended path, using the CanvasRenderingContext2D object for the line styles, and then fills the combined stroke area using the strokeStyle attribute.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/stroke

---
## Summary

Traces the intended path, using the CanvasRenderingContext2D object for the line styles, and then fills the combined stroke area using the strokeStyle attribute.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 context.stroke();
```

## Return Value

No return value

## Examples

Basic example that shows how to draw a dark green circle with a light green outline

``` js
// draw circle with dark green fill and light green outline
ctx.fillStyle = 'green';
ctx.strokeStyle = 'lime';
ctx.lineWidth = 10;
ctx.beginPath();
ctx.arc(canvas.width/2, canvas.height/2, 50, 0, Math.PI * 2, true);
ctx.closePath();
ctx.fill();
ctx.stroke();
```

Complete example that shows how to draw a dark green circle with a light green outline

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

        // draw circle with dark green fill and light green outline
        ctx.fillStyle = 'green';
        ctx.strokeStyle = 'lime';
        ctx.lineWidth = 10;
        ctx.beginPath();
        ctx.arc(canvas.width/2, canvas.height/2, 50, 0, Math.PI * 2, true);
        ctx.closePath();
        ctx.fill();
        ctx.stroke();

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

Use the [beginPath](/apis/canvas/CanvasRenderingContext2D/beginPath) method after you call the *stroke* method to close the existing path and start a new one with different properties.

## Related specifications

[HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
