---
title: fullscreenElement
notes:
  - 'Needs mobile compat'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: Element
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Exposes the current fullscreen state, returning the element that is displayed fullscreen, or null if there is no such element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/fullscreenElement

---
## <span>Summary</span>

Exposes the current fullscreen state, returning the element that is displayed fullscreen, or null if there is no such element.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var element = document.fullscreenElement;
```

## <span>Return Value</span>

Returns an object of type ElementElement

Returns the element that is displayed fullscreen, or `null` if there is no such element.

## <span>Examples</span>

``` js
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

## <span>Related specifications</span>

[W3C Fullscreen](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## <span>Related specifications</span>

[W3C fullscreen working draft](http://www.w3.org/TR/fullscreen/)

## <span>See also</span>

Tutorial: [Using the full-screen API](http://docs.webplatform.org/wiki/tutorials/using_the_full-screen_api)