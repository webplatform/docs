---
title: 'textAlign'
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
summary: 'Returns or sets the text alignment value. See return value description below.'
tags:
  - API_Object_Properties
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/textAlign

---
## Summary

Returns or sets the text alignment value. See return value description below.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.textAlign;
CanvasRenderingContext2D.textAlign = value;
```

## Return Value

Returns an object of type StringString

Must be one of the following:

-   "start" (default)
-   "end"
-   "left"
-   "right"
-   "center"

## Examples

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
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

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
