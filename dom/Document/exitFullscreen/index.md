---
title: exitFullscreen
notes:
  - 'Needs more mobile compat'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'The exitFullscreen method provides a way for exiting the fullscreen mode enabled by requestFullscreen.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/exitFullscreen

---
## Summary

The exitFullscreen method provides a way for exiting the fullscreen mode enabled by requestFullscreen.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
 document.exitFullscreen();
```

## Return Value

No return value

## Examples

``` js
//exit fullscreen on Enter key
document.addEventListener("keydown", function(e) {
  if (e.keyCode == 13) {
    document.exitFullscreen();
  }
}, false);
```

## Related specifications

[Fullscreen](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## See also

### Other articles

-   [tutorials/using\_the\_full-screen\_api](/tutorials/using_the_full-screen_api)
