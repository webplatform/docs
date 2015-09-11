---
title: CanvasPattern
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'An opaque object of the canvas API. See Notes.'
tags:
  0: API
  1: Objects
  3: Canvas
uri: apis/canvas/CanvasPattern

---
## <span>Summary</span>

An opaque object of the canvas API. See Notes.

## <span>Properties</span>

*No properties.*

## <span>Methods</span>

*No methods.*

## <span>Events</span>

*No events.*

## <span>Notes</span>

To use this object to create a pattern from a portion of an image, create a temporary clip canvas and use [drawImage](/apis/canvas/CanvasRenderingContext2D/drawImage) to extract the piece. Then, pass the tempoarary canvas to the [createPattern](/apis/canvas/CanvasRenderingContext2D/createPattern) method.

## <span>Related specifications</span>

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
