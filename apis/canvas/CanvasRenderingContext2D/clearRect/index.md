---
title: clearRect
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Clears all pixels on the canvas in the given rectangle (x, y, w, h) to transparent black.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/clearRect

---
## Summary

Clears all pixels on the canvas in the given rectangle (x, y, w, h) to transparent black.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 context.clearRect(x, y, w, h);
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

No return value

## Examples

This code example draws a filled rectangle by using fillRect and then clears the center portion by using clearRect. fillRect uses the width and height of the canvas, and clearRect uses percentages of the canvas width and height to create a frame.

``` html
<html>
<head>
<title>ClearRect example</title>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
<p>
    <button onclick="clearMe();">clear me</button>
    <button onclick="draw();">Reset</button>
</p>

<script>
    function draw() {
        var canvas = document.getElementById("MyCanvas"); // Get the canvas element.
        if (canvas.getContext) // Test for support.
        {
            var ctx = canvas.getContext("2d"); // Get the context to draw on.
            ctx.fillStyle = "black";  // Specify black as the fill color.
            ctx.fillRect(0, 0, canvas.width, canvas.height);  // Create a filled rectangle.
        }
    }
    function clearMe() {
        var canvas = document.getElementById("MyCanvas");
        if (canvas.getContext) {
            var ctx = canvas.getContext("2d");
            // Clear the center 80% of the canvas.
            ctx.clearRect(canvas.width * .1, canvas.height * .1, canvas.width * .8, canvas.height * .8);
        }
    }
  </script>

</body>
</html>
```

This example shows the clearRect method alone. The x,y,width, and height of the cleared rectangle are shown as percentages of the full width and height of the canvas.

``` js
// Clear the center 80% of the canvas.
ctx.clearRect(canvas.width * .1, canvas.height * .1, canvas.width * .8, canvas.height * .8);
```

## Notes

The **clearRect** method clears the canvas to transparent black (that is, each pixel's RGBA value is equal to zero). To clear to a specific color, use the **[fillRect](/apis/canvas/CanvasRenderingContext2D/fillRect)** method.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
