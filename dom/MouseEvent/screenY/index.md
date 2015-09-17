---
title: 'screenY'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.screenY](https://developer.mozilla.org/en-US/docs/Web/API/event.screenY) Article]'
  - 'Microsoft Developer Network: [[event.screenY](http://msdn.microsoft.com/en-us/library/ie/ff974883(v=vs.85).aspx) Article]'
notes:
  - 'example required'
readiness: 'In Progress'
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
summary: 'Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the screen.'
tags:
  - API_Object_Properties
  - DOM
  - DOMEvents
  - Needs_Examples
uri: dom/MouseEvent/screenY

---
## Summary

Gets the y-coordinate of the mouse pointer, relative to the upper-left corner of the screen.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## Syntax

**Note**: This property is read-only.

``` js
var yCoordinate = event.screenY;
```

## Return Value

Returns an object of type NumberNumber

The Y coordinate of the mouse cursor.

## Notes

Screen coordinates depend on document zoom level. At 200% magnification, some user agents may report the "logical" position of a pixel as half of the distance of the same position at 100% zoom.

## Related specifications

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
