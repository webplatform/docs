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
## <span>Summary</span>

The exitFullscreen method provides a way for exiting the fullscreen mode enabled by requestFullscreen.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
 document.exitFullscreen();
```

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
//exit fullscreen on Enter key
document.addEventListener("keydown", function(e) {
  if (e.keyCode == 13) {
    document.exitFullscreen();
  }
}, false);
```

## <span>Related specifications</span>

[Fullscreen](http://www.w3.org/TR/fullscreen/#api)
:   Working Draft

## <span>See also</span>

### <span>Other articles</span>

-   [tutorials/using\_the\_full-screen\_api](/tutorials/using_the_full-screen_api)
