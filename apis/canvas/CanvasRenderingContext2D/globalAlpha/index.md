---
title: globalAlpha
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An alpha value that is applied to shapes and images before they are composited onto the canvas.'
uri: apis/canvas/CanvasRenderingContext2D/globalAlpha

---
# globalAlpha

## Summary

An alpha value that is applied to shapes and images before they are composited onto the canvas.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.globalAlpha;
CanvasRenderingContext2D.globalAlpha = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Default is 1.0.

## Examples

The following example draws a semi-transparent white circle on a green background

``` {.js}
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

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/samples/canvas-tutorial/4_3_canvas_globalalpha.html)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

