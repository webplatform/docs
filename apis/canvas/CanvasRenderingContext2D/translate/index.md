---
title: translate
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Modifies the transformation matrix of this context by adding the scaling transformation described by the arguments to the transformation matrix. The arguments represent the scale factors in the horizontal (x) and vertical (y) directions. The factors are multiples.'
uri: apis/canvas/CanvasRenderingContext2D/translate

---
# translate

## Summary

Modifies the transformation matrix of this context by adding the scaling transformation described by the arguments to the transformation matrix. The arguments represent the scale factors in the horizontal (x) and vertical (y) directions. The factors are multiples.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.translate(x, y);
```

## Parameters

### x

 Data-typeÂ
:   String

 The value to add to horizontal (or x) coordinates.

### y

 Data-typeÂ
:   String

 The value to add to vertical (or y) coordinates.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This short example translates the drawing matrixes by 50px to the right and 50px to the bottom

``` {.js}
ctx.fillStyle = "lime";
ctx.fillRect(0,0,100,100);
ctx.translate(50,50);   // move the drawing coordinates by 50 px
ctx.fillStyle = "rgba(255,0,0,0.5)";
ctx.fillRect(0,0,100,100);  // note the x/y start positions at 0 (is actually 50)
```

Full example that draws two rects, the second one 50x50px translated.

``` {.html}
<!DOCTYPE html>
<html>
<head>
  <title>Canvas Textmetrics</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d");

        ctx.fillStyle = "lime";
        ctx.fillRect(0,0,100,100);
        ctx.translate(50,50);   // move the drawing coordinates by 50 px
        ctx.fillStyle = "rgba(255,0,0,0.5)";
        ctx.fillRect(0,0,100,100);  // note the x/y start positions at 0 (is actually 50)

      }
    }
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="400" height="400">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

## Notes

The *translate* method effectively remaps the (0,0) origin on a canvas. You can specify one or both parameters. When you call a canvas method such as [lineTo](/apis/canvas/CanvasRenderingContext2D/lineTo), the translate value is added to the respective x-coordinate and y-coordinate values. *translate* does not return an error if either value or any derived value is out of the canvas dimensions.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

