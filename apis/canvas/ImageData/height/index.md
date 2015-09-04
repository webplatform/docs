---
title: height
tags:
  0: API
  1: Object
  2: Properties
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The number of rows in the image data.'
uri: apis/canvas/ImageData/height

---
# height

## Summary

The number of rows in the image data.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/canvas/ImageData](/apis/canvas/ImageData)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = ImageData.height;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">unsigned long</span></span>

## Examples

This example creates an ImageData object and reports its height, then draws the ImageData onto the canvas.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
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
```

} ctxt.putImageData(imgdata, 10, 10); \</script\>

</pre>

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

