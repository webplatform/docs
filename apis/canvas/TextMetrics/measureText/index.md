---
title: measureText
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/TextMetrics
    href: /apis/canvas/TextMetrics
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/TextMetrics
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a TextMetrics object that contains the width of the specified text.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/TextMetrics/measureText

---
## Summary

Returns a TextMetrics object that contains the width of the specified text.

Method of [apis/canvas/TextMetrics](/apis/canvas/TextMetrics)[apis/canvas/TextMetrics](/apis/canvas/TextMetrics)

## Syntax

``` js
var object = TextMetrics.measureText(text);
```

## Parameters

### text

 Data-type
:   String

 The text to measure.

## Return Value

Returns an object of type DOM NodeDOM Node

**ICanvasTextMetrics**: The width of the text, in CSS pixels.

## Examples

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
alert("measureText: " + mets);
//Returns a TextMetrics object
</script>
```

## Usage

     Use measureText on the canvas context. An example can be found on the main object page TextMetrics

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
