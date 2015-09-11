---
title: fontBoundingBoxAscent
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
summary: 'The distance from the horizontal line indicated by the textBaseline attribute to the top of the highest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/TextMetrics/fontBoundingBoxAscent

---
## <span>Summary</span>

The distance from the horizontal line indicated by the textBaseline attribute to the top of the highest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.

Property of [apis/canvas/TextMetrics](/apis/canvas/TextMetrics)[apis/canvas/TextMetrics](/apis/canvas/TextMetrics)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = TextMetrics.fontBoundingBoxAscent;
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
alert("fontBoundingBoxAscent: " + mets.fontBoundingBoxAscent);
//Use with caution: may return "undefined" even in supported browsers
</script>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
