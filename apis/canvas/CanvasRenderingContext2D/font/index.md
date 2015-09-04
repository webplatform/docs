---
title: font
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The current canvas context font and characteristics, in the manner of the CSS font property.'
uri: apis/canvas/CanvasRenderingContext2D/font

---
# font

## Summary

The current canvas context font and characteristics, in the manner of the CSS font property.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

``` {.js}
var result = CanvasRenderingContext2D.font;
CanvasRenderingContext2D.font = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

The font string can consist of any CSS font description and is analogous to the CSS *font* property. The default font is `10px sans-serif`. Values that are not CSS font values are ignored.

## Examples

The following exaple write a sample string in the canvas

``` {.js}
function draw() {
  var ctx = document.getElementById('MyCanvas').getContext('2d');

  ctx.font = "16px Times New Roman";
  ctx.fillText("Lorem ipsum", 0, 30);
}
```

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

