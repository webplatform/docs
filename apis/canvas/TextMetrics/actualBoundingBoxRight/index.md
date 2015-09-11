---
title: actualBoundingBoxRight
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/TextMetrics
    href: /apis/canvas/TextMetrics
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /apis/canvas/TextMetrics
standardization_status: 'W3C Candidate Recommendation'
summary: 'The distance parallel to the baseline from the alignment point given by the textAlign attribute to the right side of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going right from the given alignment point.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/TextMetrics/actualBoundingBoxRight

---
## <span>Summary</span>

The distance parallel to the baseline from the alignment point given by the textAlign attribute to the right side of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going right from the given alignment point.

Property of [apis/canvas/TextMetrics](/apis/canvas/TextMetrics)[apis/canvas/TextMetrics](/apis/canvas/TextMetrics)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TextMetrics.actualBoundingBoxRight;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.font = "24px Arial";
var txt = "Hello world!"
ctxt.fillText(txt, 10, 75);
var mets = ctxt.measureText(txt);
alert("actualBoundingBoxRight: " + mets.actualBoundingBoxRight);
//Use with caution: may return "undefined" even in supported browsers
</script>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
