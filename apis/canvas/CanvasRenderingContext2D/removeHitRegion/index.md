---
title: 'removeHitRegion'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Removes a previously-defined hit region.'
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
uri: apis/canvas/CanvasRenderingContext2D/removeHitRegion

---
## Summary

Removes a previously-defined hit region.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 object.removeHitRegion(options);
```

## Parameters

### options

 Data-type
:   String

 This parameter is of type *HitRegionOptions*. See Related Specifications for details.

## Return Value

No return value

## Examples

``` html
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
<p>. . .</p>
<script>
var can = document.getElementById( "myCanvas" );
var ctxt = can.getContext( "2d" );
ctxt.fillStyle = "lime";
ctxt.beginPath( );
ctxt.rect( 10, 10, 100, 100 );
ctxt.fill( );
try {
    ctxt.addHitRegion( {"id": "limeRectangle" } );
} catch( e ) {
    alert( "your browser does not support hit regions" );
}
try {
    ctxt.removeHitRegion( {"id": "limeRectangle" } );
} catch( e ) {
    alert( "your browser does not support hit regions" );
}
</script>
```

## Notes

A *hit region* is an arbitrary rectangular area on the canvas that responds to user events, with the goal of simplifying event detection.

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation
