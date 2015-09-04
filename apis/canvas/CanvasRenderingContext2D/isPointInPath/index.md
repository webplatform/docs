---
title: isPointInPath
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns true if the point given by the x and y coordinates passed to the method, when treated as coordinates in the canvas coordinate space unaffected by the current transformation, is inside the intended path as determined by the non-zero winding number rule; returns false otherwise.  If either of the arguments is infinite or NaN, then the method returns false.'
uri: apis/canvas/CanvasRenderingContext2D/isPointInPath

---
# isPointInPath

## Summary

Returns true if the point given by the x and y coordinates passed to the method, when treated as coordinates in the canvas coordinate space unaffected by the current transformation, is inside the intended path as determined by the non-zero winding number rule; returns false otherwise. If either of the arguments is infinite or NaN, then the method returns false.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.isPointInPath(x, y);
```

## Parameters

### x

 Data-typeÂ
:   Number

 The x-coordinate to test.

### y

 Data-typeÂ
:   Number

 The y-coordinate to test.

## Return Value

Returns an object of type DOM Node.

Type: **VARIANT\_BOOL**

This method can return one of these values.

Return value
:   Description
false
:   The point is not in the current path.
true
:   The point is in the current path.

## Examples

This example simply tests whether a given point is in the current path (the previously defined rectangle) and alerts *true* or *false*.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.rect(20, 20, 150, 100);
alert(ctxt.isPointInPath(30,50));
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

