---
title: 'quadraticCurveTo'
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
summary: 'Ensures there is a subpath for (cpx, cpy), then connects the last point in the subpath to the given point (x, y) using a quadratic Bézier curve with control point (cpx, cpy), and then adds the given point (x, y) to the subpath.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/quadraticCurveTo

---
## Summary

Ensures there is a subpath for (cpx, cpy), then connects the last point in the subpath to the given point (x, y) using a quadratic Bézier curve with control point (cpx, cpy), and then adds the given point (x, y) to the subpath.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.quadraticCurveTo(cp1x, cp1y, x, y);
```

## Parameters

### cp1x

 Data-type
:   Number

 The x-coordinate of the Bézier control point.

### cp1y

 Data-type
:   Number

 The y-coordinate of the Bézier control point.

### x

 Data-type
:   Number

 The x-coordinate of the point to add to the current path.

### y

 Data-type
:   Number

 The y-coordinate of the point to add to the current path.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.beginPath();
ctxt.moveTo(50,50);
ctxt.quadraticCurveTo(50,100,200,50);
ctxt.stroke();
</script>
```

## Notes

A quadratic Bézier curve requires two points. The first is a control point that is used in the quadratic Bézier calculation and the second is the ending point for the curve. The starting point for the curve is the last point in the existing current subpath. If a path does not exist, use the *beginPath* and *moveTo* methods to set a starting point.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
