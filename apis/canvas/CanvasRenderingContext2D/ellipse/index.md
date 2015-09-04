---
title: ellipse
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Not Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Experimental, subject to change or removal; deletion candidate.'
summary: "Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.\n"
uri: apis/canvas/CanvasRenderingContext2D/ellipse

---
# ellipse

## Summary

Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.

**Experimental, subject to change or removal; deletion candidate.**

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.ellipse(x, y, radiusX, radiusY, rotation, startAngle, endAngle, anticlockwise);
```

## Parameters

### x

 Data-typeÂ
:   Number

 The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### y

 Data-typeÂ
:   Number

 The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### radiusX

 Data-typeÂ
:   Number

 The x-coordinate, in pixels, from the point (x,y) that the arc's path follows.

### radiusY

 Data-typeÂ
:   Number

 The y-coordinate, in pixels, from the point (x,y) that the arc's path follows.

### rotation

 Data-typeÂ
:   Number

 The rotation, in radians, the semi-major axis is inclined clockwise from the x-axis.

### startAngle

 Data-typeÂ
:   Number

 The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.

### endAngle

 Data-typeÂ
:   Number

 The starting angle, in radians.

### anticlockwise

 Data-typeÂ
:   Boolean

*true*: The arc is drawn in a counterclockwise direction from start to end.

*false*: The arc is drawn in a clockwise direction from start to end.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
IndexSizeError
:   The specified radius value is negative.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

