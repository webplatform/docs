---
title: scrollBy
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/scrollBy

---
## <span>Summary</span>

Causes the window to scroll relative to the current scrolled position by the specified x- and y-pixel offset.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
 window.scrollBy(/* see parameter list */);
```

## <span>Parameters</span>

### <span>x</span>

 Data-type
:   Number

**Integer** that specifies the horizontal scroll offset, in pixels. Positive values scroll the window right, and negative values scroll it left.

### <span>y</span>

 Data-type
:   Number

**Integer** that specifies the vertical scroll offset, in pixels. Positive values scroll the window down, and negative values scroll it up.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
// scroll one page
window.scrollBy(0, window.innerHeight);
```

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.