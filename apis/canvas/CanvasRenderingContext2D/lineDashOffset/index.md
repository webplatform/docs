---
title: lineDashOffset
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the number of pixels to offset the dash pattern.'
uri: apis/canvas/CanvasRenderingContext2D/lineDashOffset

---
# lineDashOffset

## Summary

Specifies the number of pixels to offset the dash pattern.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.lineDashOffset;
CanvasRenderingContext2D.lineDashOffset = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Default is 0.

## Examples

This example sets line dash parameters and draws a dashed line across the canvas, using an offset of 3px. The effect of the offset is difficult to see without comparing to the un-offset version. lineDashOffset is often used to achieve simple animation, as in the so-called "marching ants" line effect.

``` {.html}
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

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

