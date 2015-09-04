---
title: width
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The width of an inline text box, in CSS pixels.'
uri: apis/canvas/TextMetrics/width

---
# width

## Summary

The width of an inline text box, in CSS pixels.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/TextMetrics](/apis/canvas/TextMetrics)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = TextMetrics.width;
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
alert("width: " + mets.width);
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

