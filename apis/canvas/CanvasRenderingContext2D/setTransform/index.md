---
title: 'setTransform'
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
summary: 'Resets the current transform to the identity matrix, and then invokes the transform(a, b, c, d, e, f) method with the same arguments.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/setTransform

---
## Summary

Resets the current transform to the identity matrix, and then invokes the transform(a, b, c, d, e, f) method with the same arguments.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.setTransform(a, b, c, d, e, f);
```

## Parameters

### a

 Data-type
:   any

 The m1,1 value in the matrix.

### b

 Data-type
:   any

 The m1,2 value in the matrix.

### c

 Data-type
:   any

 The m2,1 value in the matrix.

### d

 Data-type
:   any

 The m2,2 value in the matrix.

### e

 Data-type
:   any

 The delta x (dx) value in the matrix.

### f

 Data-type
:   any

 The delta y (dy) value in the matrix.

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
ctxt.fillStyle="blue";
ctxt.fillRect(0, 0, 250, 100)
//setTransform and redraw in a different color
ctxt.setTransform(1, 0.5, -0.5, 1, 30, 10);
ctxt.fillStyle="yellow";
ctxt.fillRect(0, 0, 250, 100);
</script>
```

## Notes

The transformation matrix of the current context is reset back to the identity matrix. After it is reset, the transformation matrix of the context is multipled by the matrix that the specified parameters form.

The arguments *a, b, c, d, e, f* are sometimes called *m11, m12, m21, m22, dx, dy* or *m11, m21, m12, m22, dx, dy*. Care should be taken in particular with the order of the second and third arguments (*b* and *c*) as their order varies from API to API; APIs sometimes use the notation *m12/m21* and sometimes *m21/m12* for those positions.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
