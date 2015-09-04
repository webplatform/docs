---
title: fullscreenElement
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs mobile compat'
summary: 'Exposes the current fullscreen state, returning the element that is displayed fullscreen, or null if there is no such element.'
uri: dom/Document/fullscreenElement

---
# fullscreenElement

## Summary

Exposes the current fullscreen state, returning the element that is displayed fullscreen, or null if there is no such element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var element = document.fullscreenElement;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Element</span></span>

Returns the element that is displayed fullscreen, or `null` if there is no such element.

## Examples

``` {.js}
function inFullScreen() {
  if (document.fullscreenElement == null) {
    // no element is in full-screen mode
    return false;
  }
  else {
    // an element is in full-screen mode
    return true;
  }
}
```

## Related specifications

Specification
:   Status
[W3C Fullscreen](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## Related specifications

[W3C fullscreen working draft](http://www.w3.org/TR/fullscreen/)

## See also

Tutorial: [Using the full-screen API](http://docs.webplatform.org/wiki/tutorials/using_the_full-screen_api)