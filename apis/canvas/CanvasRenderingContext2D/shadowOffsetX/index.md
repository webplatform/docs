---
title: 'shadowOffsetX'
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
summary: 'Specifies the distance that the shadow will be offset in the positive horizontal distance, in coordinate space units.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/shadowOffsetX

---
## Summary

Specifies the distance that the shadow will be offset in the positive horizontal distance, in coordinate space units.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.shadowOffsetX;
CanvasRenderingContext2D.shadowOffsetX = value;
```

## Return Value

Returns an object of type NumberNumber

## Examples

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
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

You can use positive or negative values to control the position of a shadow. If you do not specify the *shadowOffsetX* property, the default value is zero.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
