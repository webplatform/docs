---
title: drawImage
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
summary: 'Draws the specified image onto the canvas. Can be called in three ways; see Notes.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/drawImage

---
## <span>Summary</span>

Draws the specified image onto the canvas. Can be called in three ways; see Notes.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.drawImage(image, sx, sy, sw, sh, dx, dy, dw, dh);
```

## <span>Parameters</span>

### <span>image</span>

 Data-type
:   DOM Node

 An image, canvas, or video element of the pattern to use.

### <span>sx</span>

 Data-type
:   Number

 The horizontal starting value (x), in CSS pixels, relative to the source image.

### <span>sy</span>

 Data-type
:   Number

 The vertical starting value (y), in CSS pixels, relative to the source image.

### <span>sw</span>

 Data-type
:   Number

 The width of the source image, in CSS pixels, to draw onto the canvas.

### <span>sh</span>

 Data-type
:   Number

 The height of the source image, in CSS pixels, to draw onto the canvas.

### <span>dx</span>

 Data-type
:   Number

 The horizontal (x) value, in CSS pixels, where to place the image on the canvas.

### <span>dy</span>

 Data-type
:   Number

 The vertical (y) value, in CSS pixels, where to place the image on the canvas.

### <span>dw</span>

 Data-type
:   Number

 The destination width value, in CSS pixels, to use when drawing the image to the canvas.

### <span>dh</span>

 Data-type
:   Number

 The destination height value, in CSS pixels, to use when drawing the image to the canvas.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|TypeMismatchError|The *image* parameter is not an img object, canvas element, or video element.|
|InvalidStateError \_ERR|The *image* parameter does not contain image data.|
|IndexSizeError|The numeric arguments are not valid (for example, the destination is a 0x0 rectangle).|
|SecurityError|The img or video element is not of the same origin or domain as the document that owns the canvas element.|

## <span>Examples</span>

This example uses the most straightforward syntax, simply drawing an existing page image onto the canvas.

``` html
<img id="clock" src="clock.jpg" width="200" height="100" style="visibility:hidden"/>
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var image = document.getElementById("clock");
ctxt.drawImage(image, 10, 10);
</script>
```

## <span>Notes</span>

The **drawImage** method provides three ways to draw an image onto a canvas, depending on how you use the optional parameters:

-   drawImage(*image*,*dx*,*dy*) copies an image exactly to the canvas at the location that the *dx* and *dy* parameters specify.
-   drawImage(*image*,*dx*,*dy*,*dw*,*dh*) copies an image to the canvas by using the *dw* and *dh* parameters to stretch or reduce the image. This option is similar to the size attributes on an **img** tag.
-   drawImage(*image*,*sx*,*sy*,*sw*,*sh*,*dx*,*dy*,*dw*,*dh*) copies all or part of a source image to the canvas. You can place and size the destination image by using the destination parameters.

If you do not specify the *dw* and *dh* parameters, they equal the values of *sw* and *sh*. One CSS pixel in the image is treated as one unit in the canvas coordinate space.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
