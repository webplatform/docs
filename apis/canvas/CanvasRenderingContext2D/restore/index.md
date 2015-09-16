---
title: restore
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Pops the top entry from the drawing state stack, and reset the drawing state it describes. If there is no saved state, the method does nothing.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/restore

---
## Summary

Pops the top entry from the drawing state stack, and reset the drawing state it describes. If there is no saved state, the method does nothing.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.restore();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.rect(50,50,125,75);
ctxt.stroke();
ctxt.save();
ctxt.restore();
</script>
```

## Notes

Use the *restore* method to retrieve a context state previously saved with the [save](/apis/canvas/CanvasRenderingContext2D/save) method. Affects the following states and attributes:

-   The current transformation matrix
-   The current clipping region
-   The current values of the following attributes:
    -   *strokeStyle*
    -   *fillStyle*
    -   *globalAlpha*
    -   *lineWidth*
    -   *lineCap*
    -   *lineJoin*
    -   *miterLimit*
    -   *shadowOffsetX*
    -   *shadowBlur*
    -   *shadowColor*
    -   *globalCompositeOperation*
    -   *font*
    -   *textAlign*
    -   *textBaseline*

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
