---
title: createPattern
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
summary: 'Returns a CanvasPattern object that uses the given image and repeats in the direction(s) given by the repetition argument.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/createPattern

---
## <span>Summary</span>

Returns a CanvasPattern object that uses the given image and repeats in the direction(s) given by the repetition argument.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## <span>Syntax</span>

``` js
var object = object.createPattern(image, repetition);
```

## <span>Parameters</span>

### <span>image</span>

 Data-type
:   DOM Node

 An image, canvas, or video element of the pattern to use. If the image has no image data, throws an *InvalidStateError* exception. If the image is not yet fully decoded, the method returns null.

### <span>repetition</span>

 Data-type
:   any

 The direction of repetition. The allowed values for repetition are:

-   "repeat" (both directions; default)
-   "repeat-x" (horizontal only)
-   "repeat-y" (vertical only)
-   "no-repeat" (neither).

If the parameter does not match one of the allowed values, the method throws a *SyntaxError* exception.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

**CanvasPattern**

The pattern object to use as a *fill style* together with a *CanvasRenderingContext2D* object.

## <span>Examples</span>

This example uses an image in the page (repeated in both directions) as a pattern, then places a rectangle filled with that pattern onto the canvas.

``` html
<img id="qmark" src="qmark.png" width="16px" height="16px" style="visibility:hidden"/>
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
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

## <span>Notes</span>

If the *repetition* parameter equals null or an empty string, the method defaults to "repeat".

## <span>Related specifications</span>

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
