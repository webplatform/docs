---
title: x
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Gets the x-coordinate of the mouse cursor, relative to the last positioned ancestor element.'
uri: dom/MouseEvent/x

---
# x

## Summary

Gets the x-coordinate of the mouse cursor, relative to the last positioned ancestor element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var xCoordinate = event.x;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.

## Examples

This example displays the current mouse position in the console.

``` {.js}
document.body.onmousemove = function (e) { console.log('X = ' + e.x + ' Y = " + e.y); }
```

## Notes

If the event firing element is relatively positioned, then the x-coordinate from the boundary of the element is returned. If the event firing element and all of its parent elements are not relatively positioned, then the **x** property returns a coordinate relative to the **body** element. The **x** property returns a coordinate relative to the **body** element. If the mouse or finger is outside the window when the event is called, this property returns `-1`.

## Related specifications

Specification
:   Status
[CSSOM View](http://www.w3.org/TR/cssom-view/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[event.x](http://msdn.microsoft.com/en-us/library/ie/ff974658(v=vs.85).aspx) Article]

