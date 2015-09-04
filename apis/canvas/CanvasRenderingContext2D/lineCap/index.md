---
title: lineCap
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Defines the type of endings the user agent will place on the end of lines.'
uri: apis/canvas/CanvasRenderingContext2D/lineCap

---
# lineCap

## Summary

Defines the type of endings the user agent will place on the end of lines.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.lineCap;
CanvasRenderingContext2D.lineCap = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Valid values are:

-   "butt"
-   "round"
-   "square"

## Examples

The following example draws three lines with the different line endings. With blue lines showing where the normal end of the line is.

``` {.js}
function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  var lineCap = ['butt','round','square'];

  //Draw guides
  ctx.strokeStyle = '#09f';
  ctx.beginPath();
  ctx.moveTo(10,10);
  ctx.lineTo(140,10);
  ctx.moveTo(10,140);
  ctx.lineTo(140,140);
  ctx.stroke();

  // Draw lines
  ctx.strokeStyle = 'black';
  for (i=0;i<lineCap.length;i++){
    ctx.lineWidth = 15;
    ctx.lineCap = lineCap[i];
    ctx.beginPath();
    ctx.moveTo(25+i*50,10);
    ctx.lineTo(25+i*50,140);
    ctx.stroke();
  }
}
```

## Notes

The *round* and *square* styles for the *lineCap* property make the lines slightly longer. For round ends, the cap diameter equals the [lineWidth](/apis/canvas/CanvasRenderingContext2D/lineWidth) value. The *square* style adds a rectangle with a width of 1/2 of *lineWidth*. Both the *round* and *square* styles add approximately 1/2 of the current *lineWidth* value to the end of a line. You should consider this addition if your graphics accuracy is critical.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources, including ones licensed under the CC-BY-SA license.* [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)

Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/samples/canvas-tutorial/4_6_canvas_linecap.html)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

