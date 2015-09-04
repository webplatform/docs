---
title: scale
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Adds the scaling transformation described by the arguments to the transformation matrix. The x argument represents the scale factor in the horizontal direction; the y argument represents the scale factor in the vertical direction. The factors are multiples.'
uri: apis/canvas/CanvasRenderingContext2D/scale

---
# scale

## Summary

Adds the scaling transformation described by the arguments to the transformation matrix. The x argument represents the scale factor in the horizontal direction; the y argument represents the scale factor in the vertical direction. The factors are multiples.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.scale(x, y);
```

## Parameters

### x

 Data-typeÂ
:   Number

 The horizontal scaling factor, where 1 equals unity or 100% scale.

### y

 Data-typeÂ
:   Number

 The vertical scaling factor.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This basic example draws two rects, the second scaled 1.5 times

``` {.js}
ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.scale(1.5, 1.5);    // draws the second rect 2.5 times larger
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(25,25,100,100);    // note the width & height are 1.5 times bigger than 100 px
```

This full example draws two rects, the second scaled 1.5 times

``` {.html}
<!DOCTYPE html>
<html>
<head>
  <title>Canvas Example</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d");

        ctx.fillStyle = "lime";
        ctx.fillRect(0,0,100,100);
        ctx.scale(1.5, 1.5);    // draws the second rect 2.5 times larger
        ctx.fillStyle = "rgba(255,0,0,0.5)";
        ctx.fillRect(25,25,100,100);    // note the width & height are 1.5 times bigger than 100 px

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

When you create a [CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D) object, it has a transformation matrix that identifies the current state. The *scale* method modifies the transformation by multiplying the matrix by the specified factor.

For example, `context.scale(1,.5)` halves the vertical (or y-axis) values that are used in context and leaves the horizontal (or x-axis) values the same. Similarly, `context.scale(2,2)` doubles the size of the graphics.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

