---
title: createRadialGradient
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
summary: 'Returns a radial CanvasGradient initialized with the two specified circles. This effectively creates a cone, touched by the two circles defined in the creation of the gradient, with the part of the cone before the start circle (0.0) using the color of the first offset, the part of the cone after the end circle (1.0) using the color of the last offset, and areas outside the cone (untouched by the gradient) transparent black.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/createRadialGradient

---
## Summary

Returns a radial CanvasGradient initialized with the two specified circles. This effectively creates a cone, touched by the two circles defined in the creation of the gradient, with the part of the cone before the start circle (0.0) using the color of the first offset, the part of the cone after the end circle (1.0) using the color of the last offset, and areas outside the cone (untouched by the gradient) transparent black.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.createRadialGradient(x0, y0, r0, x1, y1, r1);
```

## Parameters

### x0

 Data-type
:   Number

 The x-coordinate of the starting circle of the gradient.

### y0

 Data-type
:   Number

 The y-coordinate of the starting circle of the gradient.

### r0

 Data-type
:   Number

 The radius of the starting circle.

### x1

 Data-type
:   Number

 The x-coordinate of the ending circle of the gradient.

### y1

 Data-type
:   Number

 The y-coordinate of the ending circle of the gradient.

### r1

 Data-type
:   Number

 The radius of the ending circle.

## Return Value

Returns an object of type DOM NodeDOM Node

A **CanvasGradient** object that represents the radial gradient.

## Examples

This example creates a radial gradient, fading from yellow to red, and then places a rectangle filled with the gradient onto the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var grdt = ctxt.createRadialGradient(150, 75, 10, 100, 50, 150);
grdt.addColorStop(0, "yellow");
grdt.addColorStop(1, "red");
ctxt.fillStyle = grdt;
ctxt.fillRect(10, 10, 275, 125);
</script>
```

## Notes

You can use radial gradients together with the *fillText* or *fillRect* method.

## Related specifications

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
