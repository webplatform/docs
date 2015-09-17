---
title: 'canvas'
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
summary: 'A (read-only) reference to the canvas element that the CanvasRenderingContext2D object was created for.'
tags:
  - API_Object_Properties
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/canvas

---
## Summary

A (read-only) reference to the canvas element that the CanvasRenderingContext2D object was created for.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

**Note**: This property is read-only.

``` js
var result = CanvasRenderingContext2D.html/elements/canvas;
```

## Return Value

Returns an object of type ObjectObject

## Examples

This example gets the **id** of the canvas object for which the 2D context was created.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid black;"></canvas>
<p>. . .</p>
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

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
