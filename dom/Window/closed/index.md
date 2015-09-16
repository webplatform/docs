---
title: 'closed'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[window.closed](https://developer.mozilla.org/en-US/docs/Web/API/Window.closed) Article]'
  - 'Microsoft Developer Network: [[closed Property](http://msdn.microsoft.com/en-us/library/ie/ms533574(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/Window
summary: 'This read-only property indicates whether the referenced window is closed or not.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/closed

---
## Summary

This read-only property indicates whether the referenced window is closed or not.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

**Note**: This property is read-only.

``` js
var result = window.closed;
```

## Return Value

Returns an object of type BooleanBoolean

## Examples

``` js
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
