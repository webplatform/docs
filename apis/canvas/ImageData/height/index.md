---
title: height
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
    value: 'unsigned long'
    href: /apis/canvas/ImageData
standardization_status: 'W3C Candidate Recommendation'
summary: 'The number of rows in the image data.'
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
uri: apis/canvas/ImageData/height

---
## Summary

The number of rows in the image data.

Property of [apis/canvas/ImageData](/apis/canvas/ImageData)[apis/canvas/ImageData](/apis/canvas/ImageData)

## Syntax

**Note**: This property is read-only.

``` js
var result = ImageData.height;
```

## Return Value

Returns an object of type unsigned longunsigned long

## Examples

This example creates an ImageData object and reports its height, then draws the ImageData onto the canvas.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var imgdata = ctxt.createImageData(150, 100);
alert(imgdata.height); // 100
for (var i = 0; i < imgdata.data.length; i += 4) {
  imgdata.data[i+0] = 255;
  imgdata.data[i+1] = 255;
  imgdata.data[i+2] = 0;
  imgdata.data[i+3] = 128;
}
ctxt.putImageData(imgdata, 10, 10);
</script>
```

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
