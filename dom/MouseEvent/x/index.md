---
title: x
attributions:
  - 'Microsoft Developer Network: [[event.x](http://msdn.microsoft.com/en-us/library/ie/ff974658(v=vs.85).aspx) Article]'
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
summary: 'Gets the x-coordinate of the mouse cursor, relative to the last positioned ancestor element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/MouseEvent/x

---
## <span>Summary</span>

Gets the x-coordinate of the mouse cursor, relative to the last positioned ancestor element.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var xCoordinate = event.x;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

Gets the x-coordinate of the mouse pointer, relative to the last positioned ancestor element.

## <span>Examples</span>

This example displays the current mouse position in the console.

``` js
document.body.onmousemove = function (e) { console.log('X = ' + e.x + ' Y = " + e.y); }
```

## <span>Notes</span>

If the event firing element is relatively positioned, then the x-coordinate from the boundary of the element is returned. If the event firing element and all of its parent elements are not relatively positioned, then the **x** property returns a coordinate relative to the **body** element. The **x** property returns a coordinate relative to the **body** element. If the mouse or finger is outside the window when the event is called, this property returns `-1`.

## <span>Related specifications</span>

[CSSOM View](http://www.w3.org/TR/cssom-view/)
:   Working Draft
