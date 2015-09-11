---
title: strokeText
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Renders the given text at the given (x, y) coordinates, ensuring that the text isn''t wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/strokeText

---
## <span>Summary</span>

Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
 context.strokeText(text, x, y, maxWidth);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 The text characters to paint on the canvas.

### <span>x</span>

 Data-type
:   Number

 The horizontal coordinate to start painting the text relative to the canvas.

### <span>y</span>

 Data-type
:   Number

 The vertical coordinate of the baseline for the text to start painting, relative to the canvas.

### <span>maxWidth</span>

 Data-type
:   Number

(Optional)

The maximum possible text width. If the value is less than [width](/apis/canvas/TextMetrics/width), the text is scaled to fit.

## <span>Return Value</span>

No return value

## <span>Examples</span>

Short example of drawing an outline text

``` js
ctx.strokeStyle = 'white';
ctx.strokeText("Hello World!", canvas.width/2, canvas.height/2, maxWidth);
```

Full example of drawing an outline text

``` html
<!DOCTYPE html>
<html>
<head>
  <title>Canvas Example</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d");

        // clear background
        ctx.fillStyle = 'black';
        ctx.fillRect(0, 0, canvas.width, canvas.height);
        // draw text
        var text = "Hello World!";
        ctx.font = '3em Arial';
        ctx.textAlign = 'center';
        ctx.textBaseline = 'center';
        ctx.fillStyle = 'none';
        ctx.strokeStyle = 'white';
        // draw Hello World
        ctx.strokeText(text, canvas.width/2, canvas.height/2, canvas.width, canvas.height);

      }
    }
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
