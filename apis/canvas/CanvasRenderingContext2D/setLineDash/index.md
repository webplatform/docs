---
title: 'setLineDash'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
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
summary: 'Sets the line dash properties for the stroke.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/setLineDash

---
## Summary

Sets the line dash properties for the stroke.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.setLineDash(sequence);
```

## Parameters

### sequence

 Data-type
:   Array

 An array of integers that specifies the length of each "on" and "off" segment.

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

This example sets line dash parameters and draws a dashed line across the canvas; it then retrieves the line dash parameters used and writes them into the document.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
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

}
</script>
```

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
