---
title: getLineDash
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets the line dash properties for the stroke, as an array.'
uri: apis/canvas/CanvasRenderingContext2D/getLineDash

---
# getLineDash

## Summary

Gets the line dash properties for the stroke, as an array.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.getLineDash();
```

## Return Value

Returns an object of type DOM Node.

An array of integers that specifies the length of each "on" and "off" segment.

## Examples

This example sets line dash parameters and draws a dashed line across the canvas; it then retrieves the line dash parameters used and writes them into the document.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.setLineDash([10, 15]);
ctxt.beginPath();
ctxt.moveTo(0,75);
ctxt.lineTo(300, 75);
ctxt.stroke();
var ldash = ctxt.getLineDash();
for (var i=0; i<ldash.length; i++) {

 document.write(ldash[i] + " ");
```

} \</script\>

</pre>

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

