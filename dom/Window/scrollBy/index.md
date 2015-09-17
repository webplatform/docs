---
title: 'scrollBy'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[scrollBy](https://developer.mozilla.org/en-US/docs/Web/API/Window.scrollBy) Article]'
  - 'Microsoft Developer Network: [[scrollBy Method](http://msdn.microsoft.com/en-us/library/ie/ms536728(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Causes the window to scroll relative to the current scrolled position by the specified x- and y-pixel offset. '
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/scrollBy

---
## Summary

Causes the window to scroll relative to the current scrolled position by the specified x- and y-pixel offset.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.scrollBy(/* see parameter list */);
```

## Parameters

### x

 Data-type
:   Number

**Integer** that specifies the horizontal scroll offset, in pixels. Positive values scroll the window right, and negative values scroll it left.

### y

 Data-type
:   Number

**Integer** that specifies the vertical scroll offset, in pixels. Positive values scroll the window down, and negative values scroll it up.

## Return Value

No return value

## Examples

``` js
// scroll one page
window.scrollBy(0, window.innerHeight);
```

### Syntax

### Standards information

There are no standards that apply here.
