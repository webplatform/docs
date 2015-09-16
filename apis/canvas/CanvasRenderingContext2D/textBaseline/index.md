---
title: 'textBaseline'
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
    value: String
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns or sets the baseline value. See return value description below.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/textBaseline

---
## Summary

Returns or sets the baseline value. See return value description below.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.textBaseline;
CanvasRenderingContext2D.textBaseline = value;
```

## Return Value

Returns an object of type StringString

Must be one of the following:

-   "top" - The top of the em square
-   "hanging" - The hanging baseline
-   "middle" - The middle of the em square
-   "alphabetic" - The alphabetic baseline (default)
-   "ideographic" - The ideographic baseline
-   "bottom" - The bottom of the em square

## Examples

``` html
<canvas id="myCanvas" width="400" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
//draw a horizontal line across the canvas
ctxt.strokeStyle="green";
ctxt.moveTo(0,75);
ctxt.lineTo(400,75);
ctxt.stroke();
//set the font
ctxt.font="16px Arial"
//show words on the line with different textBaseline values
ctxt.textBaseline="top";
ctxt.fillText("TOP",5,75);
ctxt.textBaseline="bottom";
ctxt.fillText("BOTTOM",50,75);
ctxt.textBaseline="middle";
ctxt.fillText("MIDDLE",120,75);
ctxt.textBaseline="alphabetic";
ctxt.fillText("ALPHABETIC",190,75);
ctxt.textBaseline="hanging";
ctxt.fillText("HANGING",290,75);
</script>
```

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
