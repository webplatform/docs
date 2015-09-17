---
title: 'rect'
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
summary: 'Creates a new subpath containing just the four points (x, y), (x+w, y), (x+w, y+h), (x, y+h), with those four points connected by straight lines, then marks the subpath as closed. It then creates a new subpath with the point (x, y) as the only point in the subpath.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/rect

---
## Summary

Creates a new subpath containing just the four points (x, y), (x+w, y), (x+w, y+h), (x, y+h), with those four points connected by straight lines, then marks the subpath as closed. It then creates a new subpath with the point (x, y) as the only point in the subpath.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.rect(x, y, w, h);
```

## Parameters

### x

 Data-type
:   Number

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### y

 Data-type
:   Number

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### w

 Data-type
:   Number

 The width, in pixels, of the rectangle in relation to the coordinates of the canvas.

### h

 Data-type
:   Number

 The height, in pixels, of the rectangle in relation to the coordinates of the canvas.

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
</script>
```

## Notes

The *rect* method creates a closed path for the rectangle and then starts a new subpath at the point (*x*, *y*). You can fill the rectangle by using the *fillStyle* property and the *fill* method.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
