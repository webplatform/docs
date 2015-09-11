---
title: data
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/ImageData
    href: /apis/canvas/ImageData
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /apis/canvas/ImageData
standardization_status: 'W3C Candidate Recommendation'
summary: 'Initialized to a Uint8ClampedArray object. The Uint8ClampedArray object must use a Canvas Pixel ArrayBuffer for its storage, and must have a zero start offset and a length equal to the length of its storage, in bytes.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/ImageData/data

---
## <span>Summary</span>

Initialized to a Uint8ClampedArray object. The Uint8ClampedArray object must use a Canvas Pixel ArrayBuffer for its storage, and must have a zero start offset and a length equal to the length of its storage, in bytes.

Property of [apis/canvas/ImageData](/apis/canvas/ImageData)[apis/canvas/ImageData](/apis/canvas/ImageData)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = ImageData.html/elements/data;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

## <span>Examples</span>

This example creates an ImageData object, then sets all its data pixels to yellow (at half intensity), then puts the object onto the canvas at a specified position.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var imgdata = ctxt.createImageData(150, 100);
for (var i = 0; i < imgdata.data.length; i += 4) {

   imgdata.data[i+0] = 255;
   imgdata.data[i+1] = 255;
   imgdata.data[i+2] = 0;
   imgdata.data[i+3] = 128;

}
ctxt.putImageData(imgdata, 10, 10);
</script>
```

## <span>Notes</span>

An image is organized by pixels with four values per pixel: red, green, blue, and alpha. To access a specific pixel, use the formula `((canvas.width * y)+ x) *4`, where *x* and *y* are the row and offset in the image.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
