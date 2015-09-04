---
title: closed
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'This read-only property indicates whether the referenced window is closed or not.'
uri: dom/Window/closed

---
# closed

## Summary

This read-only property indicates whether the referenced window is closed or not.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = window.closed;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

## Examples

``` {.js}
var popupWindow = null;

function refreshPopupWindow() {
  if (popupWindow && !popupWindow.closed) {
    // popupWindow is open, refresh it
    popupWindow.location.reload(true);
  } else {
    // Open a new popup window
    popupWindow = window.open("popup.html","dataWindow");
  }
}
```

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[window.closed](https://developer.mozilla.org/en-US/docs/Web/API/Window.closed) Article]

Portions of this content come from the Microsoft Developer Network: [[closed Property](http://msdn.microsoft.com/en-us/library/ie/ms533574(v=vs.85).aspx) Article]

