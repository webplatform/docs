---
title: fillText
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Renders the given text at the given (x, y) coordinates, ensuring that the text isn''t wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.'
uri: apis/canvas/CanvasRenderingContext2D/fillText

---
# fillText

## Summary

Renders the given text at the given (x, y) coordinates, ensuring that the text isn't wider than maxWidth (if specified), using the current font, textAlign, and textBaseline values.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.fillText(text, x, y, maxWidth);
```

## Parameters

### text

 Data-typeÂ
:   String

 The text characters to paint on the canvas.

### x

 Data-typeÂ
:   Number

 The horizontal coordinate to start painting the text at, relative to the canvas.

### y

 Data-typeÂ
:   Number

 The vertical coordinate to start painting the text, relative to the canvas.

### maxWidth

 Data-typeÂ
:   Number

*(Optional)*

The maximum possible text width. If the value is less than the [width](/apis/canvas/TextMetrics/width) property, the text is scaled to fit.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
SecurityError
:   The current font is not of the same origin or domain as the document that owns the canvas element.

## Examples

This example sets a font for upcoming text, then places the value of a string variable onto the canvas.

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var text = "Hello, world.";
ctxt.font="24px Verdana";
ctxt.fillText(text, 50, 75);
</script>
```

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

