---
title: strokeStyle
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'The current style for stroking shapes. The style can be a CanvasGradient, a CanvasPattern, or a string containing a CSS color.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/strokeStyle

---
## <span>Summary</span>

The current style for stroking shapes. The style can be a CanvasGradient, a CanvasPattern, or a string containing a CSS color.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var result = CanvasRenderingContext2D.strokeStyle;
CanvasRenderingContext2D.strokeStyle = value;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

Default is black.

## <span>Examples</span>

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.strokeStyle="green";
ctxt.strokeRect(20,30,150,75);
</script>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
