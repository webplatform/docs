---
title: canvas
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'A (read-only) reference to the canvas element that the CanvasRenderingContext2D object was created for.'
uri: apis/canvas/CanvasRenderingContext2D/canvas

---
# canvas

## Summary

A (read-only) reference to the canvas element that the CanvasRenderingContext2D object was created for.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = CanvasRenderingContext2D.canvas;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

This example gets the **id** of the canvas object for which the 2D context was created.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid black;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "#0000ff";
ctxt.fillRect(10,10,150,75);
alert(ctxt.canvas.id); // returns "myCanvas"
</script>
```

## Notes

You can use the *canvas* property to access the *canvas* element from functions where you passed in only the current [CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D) object.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

