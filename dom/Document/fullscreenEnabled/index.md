---
title: fullscreenEnabled
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs mobile compat'
summary: 'Exposes the current document''s fullscreen capability, returning true if the document can display elements in fullscreen, or false if not.'
uri: dom/Document/fullscreenEnabled

---
# fullscreenEnabled

## Summary

Exposes the current document's fullscreen capability, returning true if the document can display elements in fullscreen, or false if not.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = document.fullscreenEnabled;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Returns true if document has the ability to display elements fullscreen, or false otherwise.

## Examples

``` {.js}
function canDisplayFullScreen() {
  if (document.fullscreenEnabled) {
    // document can display elements in full-screen mode
    return true;
  }
  else {
    // document cannot display elements in full-screen mode
    return false;
  }
}
```

## Related specifications

Specification
:   Status
[W3C Fullscreen Module](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## See also

Tutorial: [Using the full-screen API](http://docs.webplatform.org/wiki/tutorials/using_the_full-screen_api)