---
title: addColorStop
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasGradient
    href: /apis/canvas/CanvasGradient
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/canvas/CanvasGradient
standardization_status: 'W3C Candidate Recommendation'
summary: 'Adds a new stop to a gradient. If offset is less than 0 or greater than 1 then an IndexSizeError exception must be thrown. If the color cannot be parsed as a CSS &lt;color&gt; value, then a SyntaxError exception must be thrown. Otherwise the gradient must have a new stop placed, at offset offset relative to the whole gradient, and with the color obtained by parsing color as a CSS &lt;color&gt; value.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasGradient/addColorStop

---
## <span>Summary</span>

Adds a new stop to a gradient. If offset is less than 0 or greater than 1 then an IndexSizeError exception must be thrown. If the color cannot be parsed as a CSS &lt;color&gt; value, then a SyntaxError exception must be thrown. Otherwise the gradient must have a new stop placed, at offset offset relative to the whole gradient, and with the color obtained by parsing color as a CSS &lt;color&gt; value.

Method of [apis/canvas/CanvasGradient](/apis/canvas/CanvasGradient)[apis/canvas/CanvasGradient](/apis/canvas/CanvasGradient)

## <span>Syntax</span>

``` js
var object = CanvasGradient.addColorStop(offset, color);
```

## <span>Parameters</span>

### <span>offset</span>

 Data-type
:   any

 A floating point value between 0.0 and 1.0 that represents the position between the start and end points in a gradient.

### <span>color</span>

 Data-type
:   any

 A CSS color string to display at the position that the *offset* parameter specifies.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

The following code example creates a gradient.

``` html
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript">
function draw()
{
  var canvas = document.getElementById("MyCanvas");
    if (canvas.getContext) {
      var ctx = canvas.getContext("2d");
      gradient = ctx.createLinearGradient(0, 0, canvas.width, 0);
  // Add the colors with fixed stops at 1/4 of the width.
      gradient.addColorStop("0","magenta");
      gradient.addColorStop(".25","blue");
      gradient.addColorStop(".50","green");
      gradient.addColorStop(".75","yellow");
      gradient.addColorStop("1.0","red");

      // Use the gradient.
      ctx.fillStyle = gradient;
      ctx.fillRect (0,0,300,250);
      ctx.fillRect(250,300,600,500);
    }
}
  </script>
</head>
<body>
  <canvas id="MyCanvas" width="600" height="500" border="1"> </canvas>
    <button onclick="draw()">Click me</button>
</body>
</html>
```

## <span>Notes</span>

You can call the **addColorStop** method multiple times to change a gradient. If you never call this method for [CanvasGradient](/apis/canvas/CanvasGradient), the gradient is not visible. You need to create at least one color stop to have a visible gradient.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
