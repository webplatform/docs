---
title: lineDashOffset
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the number of pixels to offset the dash pattern.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/lineDashOffset

---
## <span>Summary</span>

Specifies the number of pixels to offset the dash pattern.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var result = CanvasRenderingContext2D.lineDashOffset;
CanvasRenderingContext2D.lineDashOffset = value;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

Default is 0.

## <span>Examples</span>

This example sets line dash parameters and draws a dashed line across the canvas, using an offset of 3px. The effect of the offset is difficult to see without comparing to the un-offset version. lineDashOffset is often used to achieve simple animation, as in the so-called "marching ants" line effect.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.setLineDash([10, 15]);
ctxt.beginPath();
ctxt.lineDashOffset = 3;
ctxt.moveTo(0,75);
ctxt.lineTo(300, 75);
ctxt.stroke();
</script>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
