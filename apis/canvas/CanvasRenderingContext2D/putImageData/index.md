---
title: putImageData
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they are assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.'
uri: apis/canvas/CanvasRenderingContext2D/putImageData

---
# putImageData

## Summary

Writes data from ImageData structures back to the canvas. If any of the arguments are infinite or NaN, the method must throw a NotSupportedError exception. When the last four arguments are omitted, they are assumed to have the values 0, 0, the width member of the imagedata structure, and the height member of the imagedata structure, respectively.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.putImageData(imagedata, dx, dy, dirtyX, dirtyY, dirtyWidth, dirtyHeight);
```

## Parameters

### imagedata

 Data-typeÂ
:   any

 An *ImageData* object with an image's pixel data.

### dx

 Data-typeÂ
:   any

 The x-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### dy

 Data-typeÂ
:   any

 The y-coordinate, in pixels, of the upper-left corner of the rectangle in relation to the coordinates of the canvas.

### dirtyX

 Data-typeÂ
:   any

*(Optional)*

The horizontal (x) value, in CSS pixels, where to place the image on the canvas.

### dirtyY

 Data-typeÂ
:   any

*(Optional)*

The vertical (y) value, in CSS pixels, where to place the image on the canvas.

### dirtyWidth

 Data-typeÂ
:   any

*(Optional)*

The destination width value, in CSS pixels, to use to draw the image to the canvas.

### dirtyHeight

 Data-typeÂ
:   any

*(Optional)*

The destination height value, in CSS pixels to use to draw the image to the canvas.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
NotSupportedError
:   One of the parameters is infinite or not a number (NaN).
TypeMismatchError
:   The first parameter is not an CanvasImageData object.
SecurityError
:   The image is not of the same origin or domain as the destination.

## Examples

This example draws a solid color filled rectangle, then uses getImageData to retrieve part of the rectangle, and then uses putImageData to place that retrieved data elsewhere on the canvas.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "magenta";
ctxt.fillRect(10, 10, 75, 75);
var imgdata = ctxt.getImageData(10, 10, 30, 30);
ctxt.putImageData(imgdata, 100, 55);
</script>
```

## Notes

You can specify an optional rectangle to show only those pixels. This "dirty" rectangle refers to a section of pixels to paint. You can use this option to specify areas on an image that might change without repainting the complete image.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

