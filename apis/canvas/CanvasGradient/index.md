---
title: CanvasGradient
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An opaque object of the canvas API.'
tags:
  0: API
  1: Objects
  3: Canvas
uri: apis/canvas/CanvasGradient

---
## <span>Summary</span>

An opaque object of the canvas API.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

API Name
:   Summary

[addColorStop](/apis/canvas/CanvasGradient/addColorStop)
:   Adds a new stop to a gradient. If *offset* is less than 0 or greater than 1 then an IndexSizeError exception must be thrown. If the color cannot be parsed as a CSS \<color\> value, then a SyntaxError exception must be thrown. Otherwise the gradient must have a new stop placed, at offset *offset* relative to the whole gradient, and with the color obtained by parsing *color* as a CSS \<color\> value.

## <span>Events</span>

*No events.*

## <span>Examples</span>

The following code example creates a gradient.

``` html
<!DOCTYPE html>
<html>
<head>
  <title>Canvas gradient test</title>
  <script>
    function draw() {
      var canvas = document.getElementById("MyCanvas");
      if (canvas.getContext) {  // check for support
        var ctx = canvas.getContext("2d");

        //create a gradient object from the canvas context
        gradient = ctx.createLinearGradient(0, 0, canvas.width, 0);

        //Add the colors with fixed stops at 1/4 of the width.
        gradient.addColorStop("0", "magenta");
        gradient.addColorStop(".25", "blue");
        gradient.addColorStop(".50", "green");
        gradient.addColorStop(".75", "yellow");
        gradient.addColorStop("1.0", "red");

        //Use the gradient.
        ctx.fillStyle = gradient;
        ctx.fillRect(0, 0, 300, 250);
        ctx.fillRect(250, 300, 600, 500);
      }
    }
  </script>
</head>
<body onload="draw();">
  <canvas id="MyCanvas" width="600" height="500">This browser or document mode doesn't support canvas</canvas>
</body>
</html>
```

## <span>Notes</span>

You can create a linear or radial **CanvasGradient** object by using the **createLinearGradient** or **createRadialGradient** method. A **CanvasGradient** object must have at least one **color stop** or the gradient is not visible.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
