---
title: toDataURL
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "\nMove Candidate:   Probably should be under HTML5 canvas element. See HTML5 specification.\n\n"
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLCanvasElement
    href: /dom/HTMLCanvasElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLCanvasElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: canvas/methods/toDataURL

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLCanvasElement](/dom/HTMLCanvasElement)[dom/HTMLCanvasElement](/dom/HTMLCanvasElement)

## <span>Syntax</span>

``` js
var object = object.toDataURL(/* see parameter list */);
```

## <span>Parameters</span>

### <span>type</span>

 Data-type
:   any

 The standard MIME type for the image format to return. If you do not specify this parameter, the default value is a PNG format image.

### <span>jpegquality</span>

 Data-type
:   any

 The quality level of a JPEG image in the range of 0.0 to 1.0.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

String

The image data.

## <span>Examples</span>

The following code example draws some graphics on a canvas and then uses **toDataURL** to make an image that is assigned to an **img** object.

``` html
<!DOCTYPE html><html>
<head>
  <script type="text/javascript">
function draw()
{
// Create some graphics.
  var canvas = document.getElementById("MyCanvas");
  if (canvas.getContext)
    {
    var ctx = canvas.getContext("2d");
    ctx.fillStyle="white";
    ctx.beginPath();
    ctx.rect (5,5,300,250);
    ctx.fill();
    ctx.stroke();
    ctx.arc(150,150,100,0,Math.PI, false);
    ctx.stroke();
    }
}
function putImage()
{
  var canvas1 = document.getElementById("MyCanvas");
  if (canvas1.getContext) {
     var ctx = canvas1.getContext("2d");                // Get the context for the canvas.
     var myImage = canvas1.toDataURL("image/png");      // Get the data as an image.
  }
  var imageElement = document.getElementById("MyPix");  // Get the img object.
  imageElement.src = myImage;                           // Set the src to data from the canvas.

}
  </script>
</head>
<body onload="draw()" bgcolor="lightgray" >
      <div>
        <button onclick="putImage()">Copy graphic using toDataURL</button>
      </div>
      <div>
        <canvas id="MyCanvas" width="400" height="400" > </canvas>
      <img id="MyPix">
      </div>
  </body>
</html>
```

## <span>Notes</span>

### <span>Remarks</span>

Typical values for the *type* parameter are `image/png` or `image/jpg`.

### <span>Syntax</span>

### <span>Standards information</span>

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.8.10

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `canvas`
