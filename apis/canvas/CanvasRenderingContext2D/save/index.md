---
title: save
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Saves the current state of the context. Use the restore() method to retrieve the saved state.'
uri: apis/canvas/CanvasRenderingContext2D/save

---
# save

## Summary

Saves the current state of the context. Use the restore() method to retrieve the saved state.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.save();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
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

The *save* and [restore](/apis/canvas/CanvasRenderingContext2D/restore) methods preserve and restore the state of a context, but not specific paths or graphics. The following attributes and states are affected:

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

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

