---
title: data
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Initialized to a Uint8ClampedArray object. The Uint8ClampedArray object must use a Canvas Pixel ArrayBuffer for its storage, and must have a zero start offset and a length equal to the length of its storage, in bytes.'
uri: apis/canvas/ImageData/data

---
# data

## Summary

Initialized to a Uint8ClampedArray object. The Uint8ClampedArray object must use a Canvas Pixel ArrayBuffer for its storage, and must have a zero start offset and a length equal to the length of its storage, in bytes.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/ImageData](/apis/canvas/ImageData)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = ImageData.data;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

## Examples

This example creates an ImageData object, then sets all its data pixels to yellow (at half intensity), then puts the object onto the canvas at a specified position.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var imgdata = ctxt.createImageData(150, 100);
for (var i = 0; i < imgdata.data.length; i += 4) {

  imgdata.data[i+0] = 255;
  imgdata.data[i+1] = 255;
  imgdata.data[i+2] = 0;
  imgdata.data[i+3] = 128;
```

} ctxt.putImageData(imgdata, 10, 10); \</script\>

</pre>

## Notes

An image is organized by pixels with four values per pixel: red, green, blue, and alpha. To access a specific pixel, use the formula `((canvas.width * y)+ x) *4`, where *x* and *y* are the row and offset in the image.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

