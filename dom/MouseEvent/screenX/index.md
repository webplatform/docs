---
title: screenX
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
readiness: 'In Progress'
standardization_status: 'W3C Working Draft'
notes:
  - 'example required'
summary: 'Gets the x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen.'
uri: dom/MouseEvent/screenX

---
# screenX

## Summary

Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the screen.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/MouseEvent](/dom/MouseEvent)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var xCoordinate = event.screenX;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

The X coordinate of the mouse cursor.

**Needs Examples**: This section should include examples.

## Notes

Screen coordinates depend on the document zoom level. At 200% magnification, some user agents may report the "logical" position of a pixel as half of the distance of the same position at 100% zoom.

## Related specifications

Specification
:   Status
[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.screenX](https://developer.mozilla.org/en-US/docs/Web/API/event.screenX) Article]

Portions of this content come from the Microsoft Developer Network: [[event.screenX](http://msdn.microsoft.com/en-us/library/ie/ff974882(v=vs.85).aspx) Article]

