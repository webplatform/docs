---
title: 'miterLimit'
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
summary: 'The current miter limit ratio.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/miterLimit

---
## Summary

The current miter limit ratio.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.miterLimit;
CanvasRenderingContext2D.miterLimit = value;
```

## Return Value

Returns an object of type NumberNumber

When setting, values that are not finite values greater than zero are ignored. Default is 10.0.

## Examples

The following example shows the effect of the miterLimit

``` js
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');

  // Clear canvas
  ctx.clearRect(0,0,150,150);

  // Draw guides
  ctx.strokeStyle = '#09f';
  ctx.lineWidth   = 2;
  ctx.strokeRect(-5,50,160,50);

  // Set line styles
  ctx.strokeStyle = '#000';
  ctx.lineWidth = 10;

  // change this to see the effects
  ctx.miterLimit = 7;

  // Draw lines
  ctx.beginPath();
  ctx.moveTo(0,100);
  for (i=0;i<24;i++){
    var dy = i%2==0 ? 25 : -25 ;
    ctx.lineTo(Math.pow(i,1.5)*2,75+dy);
  }
  ctx.stroke();
  return false;
}
```

## Notes

The miter length is the distance from the point where two lines meet to the point where two lines that are drawn along the outer edges of the two lines would intersect. If the ratio of these values exceeds the *miterLimit* value, a [lineJoin](/apis/canvas/CanvasRenderingContext2D/lineJoin) miter style is not drawn.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
