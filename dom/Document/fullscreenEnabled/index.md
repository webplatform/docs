---
title: 'fullscreenEnabled'
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
    value: Boolean
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Exposes the current document''s fullscreen capability, returning true if the document can display elements in fullscreen, or false if not.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/fullscreenEnabled

---
## Summary

Exposes the current document's fullscreen capability, returning true if the document can display elements in fullscreen, or false if not.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var result = document.fullscreenEnabled;
```

## Return Value

Returns an object of type BooleanBoolean

Returns true if document has the ability to display elements fullscreen, or false otherwise.

## Examples

``` js
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

[W3C Fullscreen Module](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## See also

Tutorial: [Using the full-screen API](http://docs.webplatform.org/wiki/tutorials/using_the_full-screen_api)
