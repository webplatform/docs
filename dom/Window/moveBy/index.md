---
title: moveBy
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[moveBy](https://developer.mozilla.org/en-US/docs/Web/API/Window.moveBy) Article]'
  - 'Microsoft Developer Network: [[moveBy Method](http://msdn.microsoft.com/en-us/library/ie/ms536618(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Moves the screen position of the window by the specified x and y offset values.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/moveBy

---
## Summary

Moves the screen position of the window by the specified x and y offset values.

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.moveBy(/* see parameter list */);
```

## Parameters

### x

 Data-type
:   any

**Integer** that specifies the horizontal scroll offset in pixels. The value can be either positive or negative.

### y

 Data-type
:   any

**Integer** that specifies the vertical scroll offset in pixels. The value can be either positive or negative.

## Return Value

No return value

## Examples

``` js
function budge() {
  moveBy(10, -10);
}
```

## Notes

This method is not valid with windows created using the [**showModalDialog**](/dom/Window/showModalDialog) method. In order to move or resize a dialog window created with these methods, change the [**dialogHeight**](/dom/WindowModal/dialogHeight), [**dialogWidth**](/dom/WindowModal/dialogWidth), [**dialogTop**](/dom/WindowModal/dialogTop), and [**dialogLeft**](/dom/WindowModal/dialogLeft) properties. If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area. Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window\_Restrictions and will be forced to stay on screen. This applies to [**moveTo**](/dom/Window/moveTo), **moveBy**, [**resizeTo**](/dom/Window/resizeTo), and [**resizeBy**](/dom/Window/resizeBy) methods. **Note:**  When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information. Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled. If multiple tabs are open, this method is blocked. For information regarding tab interaction from a script, see Tabbed Browsing for Developers. Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).
