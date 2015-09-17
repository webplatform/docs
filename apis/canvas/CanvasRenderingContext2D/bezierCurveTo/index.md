---
title: 'bezierCurveTo'
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
summary: 'Ensures there is a subpath for (cp1x, cp1y), then connects the last point in the subpath to the given point (x, y) using a cubic Bézier curve with control points (cp1x, cp1y) and (cp2x, cp2y), then adds the point (x, y) to the subpath.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/bezierCurveTo

---
## Summary

Ensures there is a subpath for (cp1x, cp1y), then connects the last point in the subpath to the given point (x, y) using a cubic Bézier curve with control points (cp1x, cp1y) and (cp2x, cp2y), then adds the point (x, y) to the subpath.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y);
```

## Parameters

### cp1x

 Data-type
:   Number

 The x-coordinate of the first Bézier control point.

### cp1y

 Data-type
:   Number

 The y-coordinate of the first Bézier control point.

### cp2x

 Data-type
:   Number

 The x-coordinate of the second Bézier control point.

### cp2y

 Data-type
:   Number

 The y-coordinate of the second Bézier control point.

### x

 Data-type
:   Number

 The x-coordinate of the point to add to the current path.

### y

 Data-type
:   Number

 The y-coordinate of the point to add to the current path.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

The following code example draws a Bézier curve between two points. It also draws a reference line to display the deviation of the curve over a straight line between the beginning and ending points.

``` js
<html>
<head>
    <title>BezierCurveTo example</title>
</head>
    <body onload="beginDemo();">
        <canvas id="demo" width="400" height="400">This browser or document mode doesn't support canvas</canvas>

    <script>
        function beginDemo() {
            var canvas = document.getElementById("demo")
            if (canvas.getContext) {
                var ctx = canvas.getContext('2d');
                // Draw a straight reference line.
                ctx.beginPath();
                ctx.strokeStyle = "blue";
                ctx.moveTo(100, 100);
                ctx.lineTo(300, 100);
                ctx.stroke();
                // Draw a Bézier curve by using the same line cooridinates.
                ctx.beginPath();
                ctx.lineWidth = "3";
                ctx.strokeStyle = "black";
                ctx.moveTo(100, 100);
                ctx.bezierCurveTo(200, 200, 200, 0, 300, 100);
                ctx.stroke();
            }
        }
     </script>

    </body>
</html>
```

The following sets up a bezierCurve using a black line with a width of 3 pixels.

``` html
// Draw a Bézier curve by using the same line cooridinates.
ctx.beginPath();
ctx.lineWidth = "3";
ctx.strokeStyle = "black";
ctx.moveTo(100, 100);
ctx.bezierCurveTo(200, 200, 200, 0, 300, 100);
ctx.stroke();
```

## Notes

A cubic Bézier curve must include three points. The first two are control points and the third is the ending point for the curve. The first point on the curve is the last point in the existing current subpath. If a path does not exist, use the *beginPath* and *moveTo* methods to create a starting point.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
