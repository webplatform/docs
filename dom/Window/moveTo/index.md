---
title: 'moveTo'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[moveTo](https://developer.mozilla.org/en-US/docs/Web/API/Window.moveTo) Article]'
  - 'Microsoft Developer Network: [[moveTo Method](http://msdn.microsoft.com/en-us/library/ie/ms536626(v=vs.85).aspx) Article]'
notes:
  - 'Needs a clean up - compatibility notes should have their own appropriate section.'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Window
    href: /dom/Window
summary: 'Moves the screen position of the upper-left corner of the window to the specified x and y position'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Window/moveTo

---
## Summary

Moves the screen position of the upper-left corner of the window to the specified x and y position

Method of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
 window.moveTo(/* see parameter list */);
```

## Parameters

### x

 Data-type
:   Number

**Integer** that specifies the horizontal scroll offset in pixels. The value can be either positive or negative.

### y

 Data-type
:   Number

**Integer** that specifies the vertical scroll offset in pixels. The value can be either positive or negative.

## Return Value

No return value

## Examples

Move to the top of the screen.

``` js
function origin() {
  // moves to top left corner of screen
  window.moveTo(0, 0);
}
```

## Notes

This method is not valid with windows created using the [**showModalDialog**](/dom/Window/showModalDialog) method. In order to move or resize a dialog window created with these methods, change the [**dialogHeight**](/dom/WindowModal/dialogHeight), [**dialogWidth**](/dom/WindowModal/dialogWidth), [**dialogTop**](/dom/WindowModal/dialogTop), and [**dialogLeft**](/dom/WindowModal/dialogLeft) properties. If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area. Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window\_Restrictions and will be forced to stay on screen. This applies to **moveTo**, [**moveBy**](/dom/Window/moveBy), [**resizeTo**](/dom/Window/resizeTo), and [**resizeBy**](/dom/Window/resizeBy) methods. **Note:**  When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information. Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled. If multiple tabs are open, this method is blocked. For information regarding tab interaction from a script, see Tabbed Browsing for Developers. Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).
