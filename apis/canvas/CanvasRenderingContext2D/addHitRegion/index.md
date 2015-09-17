---
title: 'addHitRegion'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/canvas/CanvasRenderingContext2D
    href: /apis/canvas/CanvasRenderingContext2D
standardization_status: 'W3C Candidate Recommendation'
summary: 'Creates a hit region.'
tags:
  - API_Object_Methods
  - API
  - Canvas
uri: apis/canvas/CanvasRenderingContext2D/addHitRegion

---
## Summary

Creates a hit region.

Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)[apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)

## Syntax

``` js
 context.addHitRegion(options);
```

## Parameters

### options

 Data-type
:   Object

 This parameter is of type *HitRegionOptions*. It can have following members:

-   **id** ( default empty string ) Used as reference for the HitRegion ( e.g. in [MouseEvents](/dom/MouseEvent) )
-   **control** ( default null ) An element ( descendant of the canvas ) to which the event is routed

## Return Value

No return value

## Examples

simple click detection

``` js
var canvas = document.getElementById( "mycanvas" );
var ctx = canvas.getContext( "2d" );
ctx.fillStyle = "lime";
ctx.beginPath( );
ctx.rect( 10, 10, 100, 100 );
ctx.fill( );
try {
    ctx.addHitRegion( {"id": "limeRectangle" } );
} catch( e ) {
    alert( "your browser does not support hit regions" );
}
canvas.onclick = function( e ) {
    if( e.region ) {
        alert( "clicked on: " + e.region );
    }
};
```

## Related specifications

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/#hit-regions)
:   W3C Candidate Recommendation

[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Notes

A *hit region* is an arbitrary rectangular area on the canvas that responds to user events, with the goal of simplifying event detection.

