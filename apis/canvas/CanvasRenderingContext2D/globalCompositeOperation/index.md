---
title: 'globalCompositeOperation'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Sets how shapes and images are drawn onto the existing bitmap once they have had globalAlpha and the current transformation matrix applied.'
tags:
  - API_Object_Properties
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/globalCompositeOperation

---
## Summary

Sets how shapes and images are drawn onto the existing bitmap once they have had globalAlpha and the current transformation matrix applied.

Property of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var result = CanvasRenderingContext2D.globalCompositeOperation;
CanvasRenderingContext2D.globalCompositeOperation = value;
```

## Return Value

Returns an object of type StringString

Must be set to a value from the following list. In the descriptions below, the source image, *A*, is the shape or image being rendered; the destination image, *B*, is the current state of the bitmap. **Note:** Values are case-sensitive.

-   "source-atop" - A atop B. Display the source image wherever both images are opaque. Display the destination image wherever the destination image is opaque but the source image is transparent. Display transparency elsewhere.
-   "source-in" - A in B. Display the source image wherever both the source image and destination image are opaque. Display transparency elsewhere.
-   "source-out" - A out B. Display the source image wherever the source image is opaque and the destination image is transparent. Display transparency elsewhere.
-   "source-over" (default) - A over B. Display the source image wherever the source image is opaque. Display the destination image elsewhere.
-   "destination-atop" - B atop A. Same as source-atop but using the destination image instead of the source image and vice versa.
-   "destination-in" - B in A. Same as source-in but using the destination image instead of the source image and vice versa.
-   "destination-out" - B out A. Same as source-out but using the destination image instead of the source image and vice versa.
-   "destination-over" - B over A. Same as source-over but using the destination image instead of the source image and vice versa.
-   "lighter" - A plus B. Display the sum of the source image and destination image, with color values approaching 255 (100%) as a limit.
-   "copy" - A (B is ignored). Display the source image instead of the destination image.
-   "xor" - A xor B. Exclusive OR of the source image and destination image.
-   *vendorName-operationName* - Vendor-specific extensions to the list of composition operators should use this syntax.

## Examples

This example draws two pairs of overlapping rectangles using different globalCompositionOperation values. In the example, the first rectangle of each pair (green) is the *destination*; the second rectangle of each pair (yellow) is the *source*. Thus in the first **source-over** pair, yellow overlays green; in the second **destination-over** pair, green overlays yellow.

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById("myCanvas");
var ctxt = can.getContext("2d");
ctxt.fillStyle = "green";
ctxt.fillRect(20, 30, 80, 50);
ctxt.fillStyle = "yellow";
ctxt.globalCompositeOperation = "source-over";
ctxt.fillRect(50, 60, 80, 50);

ctxt.fillStyle = "green";
ctxt.fillRect(150, 30, 80, 50);
ctxt.fillStyle = "yellow";
ctxt.globalCompositeOperation = "destination-over";
ctxt.fillRect(180, 60, 80, 50);
</script>
```

## Notes

You can copy images directly, or you can apply them depending on the opacity or transparency of the images or by using an XOR operation. Values are case-sensitive. If you set an unsupported or unrecognized value, *globalCompositeOperation* retains the previous value.

## Related specifications

[W3C HTML Canvas 2D Context](http://www.w3.org/TR/2dcontext/)
:   W3C Candidate Recommendation
