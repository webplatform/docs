---
title: putImageData
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
summary: 'Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they are assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/putImageData

---
## <span>Summary</span>

Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they are assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.putImageData(imagedata, dx, dy, dirtyX, dirtyY, dirtyWidth, dirtyHeight);
```

## <span>Parameters</span>

### <span>imagedata</span>

 Data-type
:   any

 An *ImageData* object with an image's pixel data.

### <span>dx</span>

 Data-type
:   any

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### <span>dy</span>

 Data-type
:   any

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### <span>dirtyX</span>

 Data-type
:   any

(Optional)

The horizontal (x) value, in CSS pixels, where to place the image on the canvas.

### <span>dirtyY</span>

 Data-type
:   any

(Optional)

The vertical (y) value, in CSS pixels, where to place the image on the canvas.

### <span>dirtyWidth</span>

 Data-type
:   any

(Optional)

The destination width value, in CSS pixels, to use to draw the image to the canvas.

### <span>dirtyHeight</span>

 Data-type
:   any

(Optional)

The destination height value, in CSS pixels to use to draw the image to the canvas.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|NotSupportedError|One of the parameters is infinite or not a number (NaN).|
|TypeMismatchError|The first parameter is not an CanvasImageData object.|
|SecurityError|The image is not of the same origin or domain as the destination.|

## <span>Examples</span>

This example draws a solid color filled rectangle, then uses getImageData to retrieve part of the rectangle, and then uses putImageData to place that retrieved data elsewhere on the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "magenta";
ctxt.fillRect(10, 10, 75, 75);
var imgdata = ctxt.getImageData(10, 10, 30, 30);
ctxt.putImageData(imgdata, 100, 55);
</script>
```

## <span>Notes</span>

You can specify an optional rectangle to show only those pixels. This "dirty" rectangle refers to a section of pixels to paint. You can use this option to specify areas on an image that might change without repainting the complete image.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
