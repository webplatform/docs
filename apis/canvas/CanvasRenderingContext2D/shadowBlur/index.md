---
title: shadowBlur
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the level of the blurring effect. The units do not map to coordinate space units, and are not affected by the current transformation matrix.'
uri: apis/canvas/CanvasRenderingContext2D/shadowBlur

---
# shadowBlur

## Summary

Specifies the level of the blurring effect. The units do not map to coordinate space units, and are not affected by the current transformation matrix.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.shadowBlur;
CanvasRenderingContext2D.shadowBlur = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Default is 0.

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.shadowBlur=15;
ctxt.shadowColor="blue";
ctxt.fillStyle="orange";
ctxt.fillRect(30,20,100,100);
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

