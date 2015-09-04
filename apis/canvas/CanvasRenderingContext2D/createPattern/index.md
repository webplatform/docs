---
title: createPattern
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a CanvasPattern object that uses the given image and repeats in the direction(s) given by the repetition argument.'
uri: apis/canvas/CanvasRenderingContext2D/createPattern

---
# createPattern

## Summary

Returns a CanvasPattern object that uses the given image and repeats in the direction(s) given by the repetition argument.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.createPattern(image, repetition);
```

## Parameters

### image

 Data-typeÂ
:   DOM Node

 An image, canvas, or video element of the pattern to use. If the image has no image data, throws an *InvalidStateError* exception. If the image is not yet fully decoded, the method returns null.

### repetition

 Data-typeÂ
:   any

 The direction of repetition. The allowed values for repetition are:

-   "repeat" (both directions; default)
-   "repeat-x" (horizontal only)
-   "repeat-y" (vertical only)
-   "no-repeat" (neither).

If the parameter does not match one of the allowed values, the method throws a *SyntaxError* exception.

## Return Value

Returns an object of type DOM Node.

**CanvasPattern**

The pattern object to use as a *fill style* together with a *CanvasRenderingContext2D* object.

## Examples

This example uses an image in the page (repeated in both directions) as a pattern, then places a rectangle filled with that pattern onto the canvas.

``` {.html}
<img id="qmark" src="qmark.png" width="16px" height="16px" style="visibility:hidden"/>
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
var image=document.getElementById("qmark");
var patn=ctxt.createPattern(image,"repeat");
ctxt.rect(0,0,150,100);
ctxt.fillStyle=patn;
ctxt.fill();
</script>
```

## Notes

If the *repetition* parameter equals null or an empty string, the method defaults to "repeat".

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

