---
title: 'arcTo'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://gist.github.com/5034180'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Recommendation'
summary: 'Check to be sure there''s a subpath for (x1, y1). Then, the behavior depends on the arguments and the last point in the subpath. See Notes.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/arcTo

---
## Summary

Check to be sure there's a subpath for (x1, y1). Then, the behavior depends on the arguments and the last point in the subpath. See Notes.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 object.arcTo(x1, y1, x2, y2, radius);
```

## Parameters

### x1

 Data-type
:   Number

 The x-coordinate for the first tangent that intersects with the current path point.

### y1

 Data-type
:   Number

 The y-coordinate for the first tangent that intersects with the current point.

### x2

 Data-type
:   Number

 The x-coordinate for the second tangent that intersects with the *x1* and *y1* points.

### y2

 Data-type
:   Number

 The y-coordinate for the second tangent that intersects with the *x1* and *y1* points.

### radius

 Data-type
:   Number

 The radius of the arc to create.

## Return Value

No return value

## Examples

This example creates an arc

``` js
<html>
  <head>
    <title>ArcTo example</title>
  </head>

    <script type="text/javascript">
      function draw(){
        var canvas = document.getElementById("myCanvas");
        if (canvas.getContext) {
            var ctx = canvas.getContext("2d");
            // Draw the imaginary tangents in blue.
            ctx.beginPath();
            ctx.lineWidth = "3";
            ctx.strokeStyle = "blue";
            ctx.moveTo(80, 100);
            ctx.lineTo(240, 100);
            ctx.moveTo(200, 60);
            ctx.lineTo(200, 220);
            ctx.stroke();           // Draw it.

            // Create two lines that have a connecting arc that could be used as a start to a rounded rectangle.
            ctx.beginPath();
            ctx.strokeStyle = "black";
            ctx.lineWidth = "5";
            ctx.moveTo(120, 100);   // Create a starting point.
            ctx.lineTo(180, 100);   // Draw a horizontal line.
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200, 180);    // Continue with a vertical line of the rectangle.
            ctx.stroke();           // Draw it.
            // Use the translate method to move the second example down.
            ctx.translate(0, 220);   // Move all y-coordinates down 220 pixels to see more clearly.
            // Draw the imaginary tangents in blue.
            ctx.beginPath();
            ctx.strokeStyle = "blue";
            ctx.lineWidth = "3";
            ctx.moveTo(200, 60);
            ctx.lineTo(200, 220);
            ctx.moveTo(220, 80);
            ctx.lineTo(120, 180);
            ctx.stroke();
            // Create a line, move the last path point to a point below, and then create an arc.
            ctx.beginPath();
            ctx.strokeStyle = "black";
            ctx.lineWidth = "5";
            ctx.moveTo(120, 100);   // Same starting point as above.
            ctx.lineTo(180, 100);   // Same horizontal line as above.
            ctx.moveTo(180, 120);    // Move the last path point down 20 pixels.
            ctx.arcTo(200, 100, 200, 120, 20); // Create an arc.
            ctx.lineTo(200, 180);    // Continue with a vertical line of the rectangle.
            ctx.stroke();
        }
        }
          </script>
  <body onload="draw();">
    <canvas id="myCanvas" width="300" height="600">This browser or document mode doesn't support canvas</canvas>

  </body>
</html>
```

[View live example](http://gist.github.com/5034180)

## Notes

The **arcTo** method creates an arc of *radius* radius between two tangents. The first tangent is defined by an imaginary line that is drawn through the last point in a path and the point *(x1, y1)*. The second tangent is defined by an imaginary line that is drawn through the point *(x1, y1)* and the point *(x2, y2)*.

The arc is drawn between the two tangents using *radius* as the radius. **arcTo** will draw a straight line from the last point of the path to the start of the arc which lies on the tangent that contains the last point on the path and *x1* and *y1*.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
