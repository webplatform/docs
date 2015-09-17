---
title: 'scroll'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[scroll](https://developer.mozilla.org/en-US/docs/Web/API/Window.scroll) Article]'
  - 'Microsoft Developer Network: [[scroll Method](http://msdn.microsoft.com/en-us/library/ie/ms536726(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Causes the window to scroll to the specified x- and y-offset at the upper-left corner of the window.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Window/scroll

---
## Summary

Causes the window to scroll to the specified x- and y-offset at the upper-left corner of the window.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.scroll(/* see parameter list */);
```

## Parameters

### x

 Data-type
:   Number

**Integer** that specifies the horizontal scroll offset, in pixels.

### y

 Data-type
:   Number

**Integer** that specifies the vertical scroll offset, in pixels.

## Return Value

No return value

## Examples

``` html
<!-- put the 100th vertical pixel at the top of the window -->

<button onClick="scroll(0, 100);">click to scroll down 100 pixels</button>
```

## Notes

### Remarks

This method is provided for backward compatibility only. The recommended way to scroll a window is to use the [**scrollTo**](/dom/Window/scrollTo) method.
