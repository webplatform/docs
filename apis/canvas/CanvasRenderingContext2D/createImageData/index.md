---
title: createImageData
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
summary: 'Depending on how it is called, returns either an ImageData object with the given sw, sh dimensions or an ImageData object with the same dimensions as the imagedata argument. See Notes.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/createImageData

---
## <span>Summary</span>

Depending on how it is called, returns either an ImageData object with the given sw, sh dimensions or an ImageData object with the same dimensions as the imagedata argument. See Notes.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.createImageData(sw, sh, imagedata);
```

## <span>Parameters</span>

### <span>sw</span>

 Data-type
:   Number

 The width of the new object, in CSS pixels.

### <span>sh</span>

 Data-type
:   Number

 The height of the new object, in CSS pixels.

### <span>imagedata</span>

 Data-type
:   Object

 An **ImageData** object of the desired width and height.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An **ImageData** object.

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

When this method is invoked with two arguments, *sw* and *sh*, it returns an **ImageData** object representing a rectangle with a width in CSS pixels equal to the absolute magnitude of *sw* and a height in CSS pixels equal to the absolute magnitude of *sh*. When invoked with a single *imagedata* argument, it returns an **ImageData** object representing a rectangle with the same dimensions as the **ImageData** object passed as the argument. The object returned is filled with transparent black.

This method is never called with all three arguments.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
