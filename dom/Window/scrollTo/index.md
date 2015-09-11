---
title: scrollTo
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[scrollTo](https://developer.mozilla.org/en-US/docs/Web/API/Window.scrollTo) Article]'
  - 'Microsoft Developer Network: [[scrollTo Method](http://msdn.microsoft.com/en-us/library/ie/ms536731(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Scrolls the window to the specified x- and y-offset.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/scrollTo

---
## <span>Summary</span>

Scrolls the window to the specified x- and y-offset.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

``` js
 window.scrollTo(/* see parameter list */);
```

## <span>Parameters</span>

### <span>x</span>

 Data-type
:   Number

**Integer** that specifies the horizontal scroll offset, in pixels.

### <span>y</span>

 Data-type
:   Number

**Integer** that specifies the vertical scroll offset, in pixels.

## <span>Return Value</span>

No return value

## <span>Examples</span>

``` js
window.scrollTo( 0, 1000 );
```

## <span>Notes</span>

### <span>Remarks</span>

The specified offsets are relative to the upper-left corner of the window.