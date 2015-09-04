---
title: CanvasPixelArray
tags:
  0: API
  1: Objects
  3: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Specifies each pixel within a canvas''s rectangular selection, via the ImageData object''s data property. The array uses four elements to represent each pixel''s red, green, blue, and alpha channels. See Notes.'
uri: apis/canvas/CanvasPixelArray

---
# CanvasPixelArray

## Summary

Specifies each pixel within a canvas's rectangular selection, via the ImageData object's data property. The array uses four elements to represent each pixel's red, green, blue, and alpha channels. See Notes.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Notes

A Canvas Pixel ArrayBuffer is not, strictly speaking, an object of the canvas API. It is a regular ArrayBuffer object (see [Typed Array Specification, ArrayBuffer Type](http://www.khronos.org/registry/typedarray/specs/latest/#5)) whose data is represented in left-to-right, top-to-bottom order, starting with the top left, with each pixel's red, green, blue, and alpha components being given in that order for each pixel. Each component of each device pixel represented in this array must be in the range 0..255, representing the 8-bit value for that component. The components must be assigned consecutive indices starting with 0 for the top left pixel's red component.

The latest HTML specification has removed CanvasPixelArray in favor of the JavaScript Uint8ClampedArray typed array. However, as of April 2012, most browsers still returns CanvasPixelArray and there are very few implementations which return Uint8ClampedArray on ImageData.data.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/CanvasPixelArray)

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

