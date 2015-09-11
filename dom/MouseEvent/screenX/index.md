---
title: screenX
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[event.screenX](https://developer.mozilla.org/en-US/docs/Web/API/event.screenX) Article]'
  - 'Microsoft Developer Network: [[event.screenX](http://msdn.microsoft.com/en-us/library/ie/ff974882(v=vs.85).aspx) Article]'
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
summary: 'Gets the x-coordinate of the mouse pointer, relative to the  upper-left corner of the screen.'
tags:
  - API
  - Object
  - Properties
  - DOM
  - DOMEvents
uri: dom/MouseEvent/screenX

---
## <span>Summary</span>

Gets the x-coordinate of the mouse pointer, relative to the upper-left corner of the screen.

Property of [dom/MouseEvent](/dom/MouseEvent)[dom/MouseEvent](/dom/MouseEvent)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var xCoordinate = event.screenX;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

The X coordinate of the mouse cursor.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Screen coordinates depend on the document zoom level. At 200% magnification, some user agents may report the "logical" position of a pixel as half of the distance of the same position at 100% zoom.

## <span>Related specifications</span>

[DOM Level 3 Events](http://www.w3.org/TR/DOM-Level-3-Events/)
:   Working Draft
