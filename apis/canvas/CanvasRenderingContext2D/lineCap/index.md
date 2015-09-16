---
title: 'lineCap'
attributions:
  - 'This article contains content originally from external sources, including ones licensed under the CC-BY-SA license. [![cc-by-sa-small-wpd.png](/assets/public/c/c8/cc-by-sa-small-wpd.png)](http://creativecommons.org/licenses/by-sa/3.0/us/)'
  - 'Portions of this content copyright 2012 Mozilla Contributors. This article contains work licensed under the Creative Commons Attribution-Sharealike License v2.5 or later. The original work is available at Mozilla Developer Network: [Article](https://developer.mozilla.org/samples/canvas-tutorial/4_6_canvas_linecap.html)'
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
summary: 'Defines the type of endings the user agent will place on the end of lines.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/lineCap

---
## Summary

Defines the type of endings the user agent will place on the end of lines.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.lineCap;
CanvasRenderingContext2D.lineCap = value;
```

## Return Value

Returns an object of type StringString

Valid values are:

-   "butt"
-   "round"
-   "square"

## Examples

The following example draws three lines with the different line endings. With blue lines showing where the normal end of the line is.

``` js
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

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Editor's Draft
