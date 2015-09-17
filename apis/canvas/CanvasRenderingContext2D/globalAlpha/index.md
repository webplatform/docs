---
title: 'globalAlpha'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/samples/canvas-tutorial/4_3_canvas_globalalpha.html)'
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
summary: 'An alpha value that is applied to shapes and images before they are composited onto the canvas.'
tags:
  - API_Object_Properties
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/globalAlpha

---
## Summary

An alpha value that is applied to shapes and images before they are composited onto the canvas.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.globalAlpha;
CanvasRenderingContext2D.globalAlpha = value;
```

## Return Value

Returns an object of type NumberNumber

Default is 1.0.

## Examples

The following example draws a semi-transparent white circle on a green background

``` js
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  // draw background
  ctx.fillStyle = '#FD0';
  ctx.fillRect(0,0,150,150)

  //set transparency value
  ctx.globalAlpha = 0.2;

  //Draw a semi transparent circle
  ctx.beginPath();
  ctx.arc(75,75,50,0,Math.PI*2,true);
  ctx.fill();
}
```

## Notes

If you set the *globalAlpha* property to a value outside the range (including infinity or not a number (NaN)), the previous value is preserved.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
