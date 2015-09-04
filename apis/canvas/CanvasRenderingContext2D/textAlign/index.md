---
title: textAlign
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns or sets the text alignment value. See return value description below.'
uri: apis/canvas/CanvasRenderingContext2D/textAlign

---
# textAlign

## Summary

Returns or sets the text alignment value. See return value description below.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.textAlign;
CanvasRenderingContext2D.textAlign = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Must be one of the following:

-   "start" (default)
-   "end"
-   "left"
-   "right"
-   "center"

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
//draw a vertical line down the middle of the canvas
ctxt.strokeStyle="green";
ctxt.moveTo(150,0);
ctxt.lineTo(150,150);
ctxt.stroke();
//set the font
ctxt.font="16px Arial";
//show effect of textAlign values
ctxt.textAlign="start";
ctxt.fillText("START",150,40);
ctxt.textAlign="end";
ctxt.fillText("END",150,60);
ctxt.textAlign="left";
ctxt.fillText("LEFT",150,80);
ctxt.textAlign="right";
ctxt.fillText("RIGHT",150,100);
ctxt.textAlign="center";
ctxt.fillText("CENTER",150,120);
</script>
```

## Notes

The exact alignment depends on whether the direction of *HTMLCanvasElement* is left-to-right (ltr) or right-to-left (rtl). The [textBaseline](/apis/canvas/CanvasRenderingContext2D/textBaseline) value also determines the anchor point of the text.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

