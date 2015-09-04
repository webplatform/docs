---
title: fill
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Fills all the subpaths of the intended path, using fillStyle, and using the non-zero winding number rule. Open subpaths must be implicitly closed when being filled (without affecting the actual subpaths).'
uri: apis/canvas/CanvasRenderingContext2D/fill

---
# fill

## Summary

Fills all the subpaths of the intended path, using fillStyle, and using the non-zero winding number rule. Open subpaths must be implicitly closed when being filled (without affecting the actual subpaths).

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.fill(path);
```

## Parameters

### path

 Data-typeÂ
:   DOM Node

*(Optional)*

The path to be filled.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example creates a 30 x 100 rectangle on the canvas, sets a solid color fill style, and fills the rectangle.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.rect(20, 20, 50, 120);
ctxt.fillStyle = "cyan";
ctxt.fill();
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

