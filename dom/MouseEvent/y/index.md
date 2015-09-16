---
title: 'y'
attributions:
  - 'Microsoft Developer Network: [[event.y Property](http://msdn.microsoft.com/en-us/library/ie/ms535164(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/MouseEvent
    href: /dom/MouseEvent
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/MouseEvent
standardization_status: 'W3C Working Draft'
summary: 'Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/MouseEvent/y

---
## Summary

Gets the y-coordinate of the mouse pointer, relative to the last positioned ancestor element.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var yCoordinate = event.y;
```

## Return Value

Returns an object of type NumberNumber

The Y coordinate of the mouse cursor.

## Examples

This example displays the current mouse position in the browser's status window.

``` js
document.body.onmousemove = function (e) { console.log('X = ' + e.x + ' Y = " + e.y); }
```

## Notes

If the event firing element is relatively positioned, then the y-coordinate from the boundary of the element is returned. If the event firing element and all of its parent elements are not relatively positioned, then the **y** property returns a coordinate relative to the **body** element. The **y** property returns a coordinate relative to the **body** element. If the mouse or finger is outside the window at the time the event fires, this property returns -1.

## Related specifications

[CSSOM View](http://www.w3.org/TR/cssom-view/)
:   Working Draft
