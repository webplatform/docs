---
title: scrollPathIntoView
tags:
  0: API
  1: Object
  2: Methods
  4: Canvas
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Scrolls the current path into view. See Notes.'
uri: apis/canvas/CanvasRenderingContext2D/scrollPathIntoView

---
# scrollPathIntoView

## Summary

Scrolls the current path into view. See Notes.

*Method of [apis/canvas/CanvasRenderingContext2D](/apis/canvas/CanvasRenderingContext2D)*

## Syntax

``` {.js}
var object = object.scrollPathIntoView();
```

## Return Value

Returns an object of type DOM Node.

## Examples

``` {.html}
<canvas id="myCanvas" width="300" height="150" style="border:1px solid blue;"></canvas>
. . .
<script>
var can=document.getElementById("myCanvas");
var ctxt=can.getContext("2d");
ctxt.rect(50,50,125,75);
ctxt.stroke();
ctxt.scrollPathIntoView();
</script>
```

## Notes

*scrollPathIntoView()* is primarily intended for use in mobile applications, on devices with small screens. Using this method, developers can scroll into view the part of the canvas that is offscreen.

## Related specifications

Specification
:   Status
[W3C HTML Canvas 2D Specification](http://www.w3.org/TR/2012/CR-2dcontext-20121217/)
:   W3C Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

