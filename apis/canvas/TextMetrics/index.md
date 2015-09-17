---
title: 'TextMetrics'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'The TextMetrics object of the canvas API. TextMetrics retrieves numeric informations like the width of a text that is drawn onto the canvas with the current font style.'
tags:
  - API_Objects
  - API
  - Canvas
uri: apis/canvas/TextMetrics

---
## Summary

The TextMetrics object of the canvas API. TextMetrics retrieves numeric informations like the width of a text that is drawn onto the canvas with the current font style.

## Properties

[actualBoundingBoxAscent](/apis/canvas/TextMetrics/actualBoundingBoxAscent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the top of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.

[actualBoundingBoxDescent](/apis/canvas/TextMetrics/actualBoundingBoxDescent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the bottom of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going down from the given baseline.

[actualBoundingBoxLeft](/apis/canvas/TextMetrics/actualBoundingBoxLeft)
:   The distance parallel to the baseline from the alignment point given by the textAlign attribute to the left side of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going left from the given alignment point.

[actualBoundingBoxRight](/apis/canvas/TextMetrics/actualBoundingBoxRight)
:   The distance parallel to the baseline from the alignment point given by the textAlign attribute to the right side of the bounding rectangle of the given text, in CSS pixels; positive numbers indicating a distance going right from the given alignment point.

[alphabeticBaseline](/apis/canvas/TextMetrics/alphabeticBaseline)
:   The distance from the horizontal line indicated by the textBaseline attribute to the alphabetic baseline of the line box, in CSS pixels; positive numbers indicating that the given baseline is below the alphabetic baseline. (Zero if the given baseline is the alphabetic baseline.)

[emHeightAscent](/apis/canvas/TextMetrics/emHeightAscent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the top of the em square in the line box, in CSS pixels; positive numbers indicating that the given baseline is below the top of the em square (so this value will usually be positive). Zero if the given baseline is the top of the em square; half the font size if the given baseline is the middle of the em square.

[emHeightDescent](/apis/canvas/TextMetrics/emHeightDescent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the bottom of the em square in the line box, in CSS pixels; positive numbers indicating that the given baseline is below the bottom of the em square (so this value will usually be negative). (Zero if the given baseline is the top of the em square.)

[fontBoundingBoxAscent](/apis/canvas/TextMetrics/fontBoundingBoxAscent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the top of the highest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going up from the given baseline.

[fontBoundingBoxDescent](/apis/canvas/TextMetrics/fontBoundingBoxDescent)
:   The distance from the horizontal line indicated by the textBaseline attribute to the bottom of the lowest bounding rectangle of all the fonts used to render the text, in CSS pixels; positive numbers indicating a distance going down from the given baseline.

[hangingBaseline](/apis/canvas/TextMetrics/hangingBaseline)
:   The distance from the horizontal line indicated by the textBaseline attribute to the hanging baseline of the line box, in CSS pixels; positive numbers indicating that the given baseline is below the hanging baseline. (Zero if the given baseline is the hanging baseline.)

[ideographicBaseline](/apis/canvas/TextMetrics/ideographicBaseline)
:   The distance from the horizontal line indicated by the textBaseline attribute to the ideographic baseline of the line box, in CSS pixels; positive numbers indicating that the given baseline is below the ideographic baseline. (Zero if the given baseline is the ideographic baseline.)

[width](/apis/canvas/TextMetrics/width)
:   The width of an inline text box, in CSS pixels.

## Methods

[measureText](/apis/canvas/TextMetrics/measureText)
:   Returns a TextMetrics object that contains the width of the specified text.

## Events

*No events.*

## Examples

Short example of getting the width of the text drawn on the canvas (with current font styles)

``` js
var metrics = context.measureText("Hello World!");
console.log(metrics.width); // returns the width of the drawn text in CSS pixels
```

This full example draws two lines of text, the second line contains the with of the first line in pixels

``` html
<!DOCTYPE html>
<html>
<head>
  <title>Canvas Textmetrics</title>
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
        ctx.font = '32pt Arial';
        ctx.textAlign = 'center';
        ctx.textBaseline = 'center';
        ctx.fillStyle = 'white';
        // measure the text that is to be drawn
        var metrics = ctx.measureText(text);
        console.log(metrics.width);
        // draw Hello World
        ctx.fillText(text, canvas.width/2, canvas.height/2, canvas.width, canvas.height);
        // draw info
        ctx.font = '12pt Arial';
        ctx.fillText("… is " + metrics.width + "px wide", canvas.width/2, canvas.height/2+25, canvas.width, canvas.height);

      }
    }
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
