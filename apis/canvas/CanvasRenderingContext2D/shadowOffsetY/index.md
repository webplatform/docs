---
title: shadowOffsetY
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies the distance that the shadow will be offset in the positive vertical distance, in coordinate space units.'
uri: apis/canvas/CanvasRenderingContext2D/shadowOffsetY

---
# shadowOffsetY

## Summary

Specifies the distance that the shadow will be offset in the positive vertical distance, in coordinate space units.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.shadowOffsetY;
CanvasRenderingContext2D.shadowOffsetY = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.shadowBlur=15;
ctxt.shadowOffsetX=10;
ctxt.shadowOffsetY=10;
ctxt.shadowColor="blue";
ctxt.fillStyle="orange";
ctxt.fillRect(30,20,100,100);
</script>
```

## Notes

You can use positive or negative values to control the position of a shadow. If you do not specify the *shadowOffsetY* property, the default value is zero.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

