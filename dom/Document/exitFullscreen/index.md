---
title: exitFullscreen
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs more mobile compat'
summary: 'The exitFullscreen method provides a way for exiting the fullscreen mode enabled by requestFullscreen.'
uri: dom/Document/exitFullscreen

---
# exitFullscreen

## Summary

The exitFullscreen method provides a way for exiting the fullscreen mode enabled by requestFullscreen.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
 document.exitFullscreen();
```

## Return Value

No return value

## Examples

``` {.js}
//exit fullscreen on Enter key
document.addEventListener("keydown", function(e) {
  if (e.keyCode == 13) {
    document.exitFullscreen();
  }
}, false);
```

## Related specifications

Specification
:   Status
[Fullscreen](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## See also

### Other articles

-   [tutorials/using\_the\_full-screen\_api](/tutorials/using_the_full-screen_api)

