---
title: 'arc'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
code_samples:
  - 'http://result.dabblet.com/gist/5024626/e8999ad1cd338a601a3d75c139e92d8ee68b2ca3'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Draws the specified arc.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/arc

---
## Summary

Draws the specified arc.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = context.arc(x, y, radius, startAngle, endAngle, anticlockwise);
```

## Parameters

### x

 Data-type
:   Number

 The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### y

 Data-type
:   Number

 The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### radius

 Data-type
:   Number

 The radius or distance from the point (x,y) that the arc's path follows.

### startAngle

 Data-type
:   Number

 The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.

### endAngle

 Data-type
:   Number

 The ending angle, in radians.

### anticlockwise

 Data-type
:   Number

(Optional)

*true*: The arc is drawn in a counterclockwise direction from start to end.

*false*: The arc is drawn in a clockwise direction from start to end.

## Return Value

Returns an object of type StringString

Type: **string**

This method can return the following value.

|Return code|Description|
|:----------|:----------|
|IndexSizeError|The specified radius value is negative.|

## Examples

The following code example shows several different arcs.

``` html
<html>
<head>
      <title>Arc example</title>
  <script type="text/javascript">
      function curves() {
          var canvas = document.getElementById("canvas");
          if (canvas.getContext) {
              var ctx = canvas.getContext("2d");
              for (var i = 0; i < 2; i++)                            // Step through two rows.
              {
                  for (var j = 0; j < 3; j++)                        // Step through three versions.
                  {
                      ctx.beginPath();
                      var x = 25 + j * 50;               // The x-coordinate.
                      var y = 25 + i * 50;               // The y-coordinate.
                      var radius = 20;                    // The arc radius.
                      var startAngle = 0;                     // The starting point on the circle.
                      var endAngle = Math.PI + (Math.PI * j) / 2; // The end point on the circle.
                      var anticlockwise = i % 2 == 0 ? false : true; // The direction of drawing.
                      ctx.arc(x, y, radius, startAngle, endAngle, anticlockwise); // Create the arc path.
                      ctx.stroke();                               // Display the work.
                  }
              }
          }
      }// Curves
  </script>
</head>
<body onload="curves();">
  <canvas id="canvas" width="300" height="300">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

[View live example](http://result.dabblet.com/gist/5024626/e8999ad1cd338a601a3d75c139e92d8ee68b2ca3)

## Notes

If the *startAngle* and *endAngle* angles are equal, the **arc** method creates a circle. To convert degrees to radians use:

    var radians = degrees * Math.PI/180

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
