---
title: scale
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
summary: 'Adds the scaling transformation described by the arguments to the transformation matrix. The x argument represents the scale factor in the horizontal direction; the y argument represents the scale factor in the vertical direction. The factors are multiples.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/scale

---
## <span>Summary</span>

Adds the scaling transformation described by the arguments to the transformation matrix. The x argument represents the scale factor in the horizontal direction; the y argument represents the scale factor in the vertical direction. The factors are multiples.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.scale(x, y);
```

## <span>Parameters</span>

### <span>x</span>

 Data-type
:   Number

 The horizontal scaling factor, where 1 equals unity or 100% scale.

### <span>y</span>

 Data-type
:   Number

 The vertical scaling factor.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

This basic example draws two rects, the second scaled 1.5 times

``` js
ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.scale(1.5, 1.5);    // draws the second rect 2.5 times larger
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(25,25,100,100);    // note the width & height are 1.5 times bigger than 100 px
```

This full example draws two rects, the second scaled 1.5 times

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

## <span>Notes</span>

When you create a [CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D) object, it has a transformation matrix that identifies the current state. The *scale* method modifies the transformation by multiplying the matrix by the specified factor.

For example, `context.scale(1,.5)` halves the vertical (or y-axis) values that are used in context and leaves the horizontal (or x-axis) values the same. Similarly, `context.scale(2,2)` doubles the size of the graphics.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
