---
title: rotate
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
summary: 'Addd the rotation transformation described by the argument to the transformation matrix. The angle argument represents a clockwise rotation angle expressed in radians.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/rotate

---
## Summary

Addd the rotation transformation described by the argument to the transformation matrix. The angle argument represents a clockwise rotation angle expressed in radians.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.rotate(angle);
```

## Parameters

### angle

 Data-type
:   Number

 The rotation angle, in radians.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This basic example draws two rects, the second rotated 45°, converted to radians

``` js
ctx.translate(120,120);
ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.rotate((Math.PI/180) * 45); // draws the second rect 45° rotated
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(0,0,100,100);
```

This full example draws two rects, the second rotated 45°

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

        ctx.translate(120,120);
        ctx.fillStyle = "lime";
        ctx.fillRect(0,0,100,100);
        ctx.rotate((Math.PI/180) * 45); // draws the second rect 45° rotated
        ctx.fillStyle = "rgba(255,0,0,0.5)";
        ctx.fillRect(0,0,100,100);

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

Rotation is based on the current origin which is most of the time the upper left corner. Use rectWidth/-2 as an offsetX and rectHeight/-2 as offsetY to draw the rotated rect with a centered origin.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
