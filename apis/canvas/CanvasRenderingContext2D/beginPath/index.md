---
title: beginPath
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/5022033/58ee0dfab60f4ee6d22c14881d9708708f45e2b2'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Empties the list of subpaths in the context''s current default path so that it once again has zero subpaths.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/beginPath

---
## Summary

Empties the list of subpaths in the context's current default path so that it once again has zero subpaths.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 context.beginPath();
```

## Return Value

No return value

## Examples

This is a full example that uses beginPath to create two stroked lines.

``` js
<html>
<head>
    <title>Canvas beginPath example</title>
    <script>
        function beginDemo() {
            var canvas = document.getElementById("demo")
            if (canvas.getContext) {
                var ctx = canvas.getContext('2d');
                ctx.beginPath();
                ctx.lineWidth = "3";
                ctx.strokeStyle = "blue";  // This path is blue.
                ctx.moveTo(0, 0);
                ctx.lineTo(150, 150);
                ctx.lineTo(200, 150);
                ctx.stroke();
                ctx.beginPath();
                ctx.strokeStyle = "red";   // This path is red.
                ctx.moveTo(0, 0);
                ctx.lineTo(50, 150);
                ctx.stroke();           // Draw it.
            }
        }
          </script>
</head>
    <body onload="beginDemo();">
        <canvas id="demo" width="300" height="300">This browser or document mode doesn't support canvas</canvas>
  </body>
</html>
```

[View live example](http://code.webplatform.org/gist/5022033/58ee0dfab60f4ee6d22c14881d9708708f45e2b2)

This snippet shows the basis syntax for beginPath() using the canvas context.

``` js
var ctx = canvas.getContext('2d');
                ctx.beginPath();
```

## Notes

A path consists of a list of zero or more subpaths. Each subpath is a list of one or more points that are connected by straight or curved lines. Each subpath also contains a flag that indicates whether the subpath is closed. If a subpath is closed, the last point of the subpath is connected to the first point by a straight line. Subpaths that have fewer than two points are ignored when the path is painted.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
