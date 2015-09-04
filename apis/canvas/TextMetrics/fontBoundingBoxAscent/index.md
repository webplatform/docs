---
title: fontBoundingBoxAscent
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The distance from the horizontal line indicated by the textBaseline attribute to the top of the highest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.'
uri: apis/canvas/TextMetrics/fontBoundingBoxAscent

---
# fontBoundingBoxAscent

## Summary

The distance from the horizontal line indicated by the textBaseline attribute to the top of the highest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/TextMetrics](/apis/canvas/TextMetrics)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextMetrics.fontBoundingBoxAscent;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.font = "24px Arial";
var txt = "Hello world!"
ctxt.fillText(txt, 10, 75);
var mets = ctxt.measureText(txt);
alert("fontBoundingBoxAscent: " + mets.fontBoundingBoxAscent);
//Use with caution: may return "undefined" even in supported browsers
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

