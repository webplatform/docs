---
title: 'ellipse'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Experimental, subject to change or removal; deletion candidate.'
readiness: 'Not Ready'
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
summary: "Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.\n"
tags:
  - API_Object_Methods
  - API
  - Canvas
  - Needs_Examples
uri: apis/canvas/CanvasRenderingContext2D/ellipse

---
## Summary

Draws the specified ellipse. If the object's path has any subpaths, this method adds a straight line from the last point in the subpath to the start point of the arc. Then, it adds the start and end points of the arc to the subpath, and connects them with an arc.

**Experimental, subject to change or removal; deletion candidate.**

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
var object = object.ellipse(x, y, radiusX, radiusY, rotation, startAngle, endAngle, anticlockwise);
```

## Parameters

### x

 Data-type
:   Number

 The x-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### y

 Data-type
:   Number

 The y-coordinate, in pixels, for the center point of the arc in relation to the upper-left corner of the canvas rectangle.

### radiusX

 Data-type
:   Number

 The x-coordinate, in pixels, from the point (x,y) that the arc's path follows.

### radiusY

 Data-type
:   Number

 The y-coordinate, in pixels, from the point (x,y) that the arc's path follows.

### rotation

 Data-type
:   Number

 The rotation, in radians, the semi-major axis is inclined clockwise from the x-axis.

### startAngle

 Data-type
:   Number

 The starting angle, in radians, where 0 is at the 3 o'clock position of the arc's circle.

### endAngle

 Data-type
:   Number

 The starting angle, in radians.

### anticlockwise

 Data-type
:   Boolean

*true*: The arc is drawn in a counterclockwise direction from start to end.

*false*: The arc is drawn in a clockwise direction from start to end.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|IndexSizeError|The specified radius value is negative.|

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
