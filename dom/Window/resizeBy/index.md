---
title: resizeBy
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs a clean up - compatibility notes should be in their own appropriate section.'
summary: 'Changes the current size of the window by the specified x- and y-offset.'
uri: dom/Window/resizeBy

---
# resizeBy

## Summary

Changes the current size of the window by the specified x- and y-offset.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 window.resizeBy(/* see parameter list */);
```

## Parameters

### x

 Data-type�
:   Number

**Integer** that specifies the horizontal offset in pixels. The value can be either positive or negative.

### y

 Data-type�
:   Number

**Integer** that specifies the vertical offset in pixels. The value can be either positive or negative.

## Return Value

No return value

## Examples

``` {.js}
// shrink the window
window.resizeBy(-200, -200);
```

## Notes

This method is not valid with windows created using the [**showModalDialog**](/dom/Window/showModalDialog) method. In order to move or resize a dialog window created with these methods, change the [**dialogHeight**](/dom/WindowModal/dialogHeight), [**dialogWidth**](/dom/WindowModal/dialogWidth), [**dialogTop**](/dom/WindowModal/dialogTop), and [**dialogLeft**](/dom/WindowModal/dialogLeft) properties. If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area. Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window\_Restrictions and will be forced to stay on screen. This applies to [**moveTo**](/dom/Window/moveTo), [**moveBy**](/dom/Window/moveBy), [**resizeTo**](/dom/Window/resizeTo), and **resizeBy** methods. **Note:** When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information. Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled. If multiple tabs are open, this method is blocked. For information regarding tab interaction from a script, see Tabbed Browsing for Developers. Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[resizeBy](https://developer.mozilla.org/en-US/docs/Web/API/Window.resizeBy) Article]

Portions of this content come from the Microsoft Developer Network: [[resizeBy Method](http://msdn.microsoft.com/en-us/library/ie/ms536722(v=vs.85).aspx) Article]

