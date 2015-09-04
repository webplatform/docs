---
title: resizeTo
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
notes:
  - 'Needs a clean up - compatibility notes should be in their own appropriate section.'
summary: 'Sets the size of the window to the specified width and height values.'
uri: dom/Window/resizeTo

---
# resizeTo

## Summary

Sets the size of the window to the specified width and height values.

*Method of [dom/Window](/dom/Window)*

## Syntax

``` {.js}
 window.resizeTo(/* see parameter list */);
```

## Parameters

### x

 Data-type�
:   Number

**Integer** that specifies the width of the window in pixels. The value can be either positive or negative.

### y

 Data-type�
:   Number

**Integer** that specifies the height of the window in pixels. The value can be either positive or negative.

## Return Value

No return value

## Examples

``` {.js}
// function resizes the window to take up one quarter
// of the available screen.
function quarter() {
  window.resizeTo(
    window.screen.availWidth / 2,
    window.screen.availHeight / 2
  );
}
```

## Notes

### Remarks

This method is not valid with windows created using the [**showModalDialog**](/dom/Window/showModalDialog) method. In order to move or resize a dialog window created with these methods, change the [**dialogHeight**](/dom/WindowModal/dialogHeight), [**dialogWidth**](/dom/WindowModal/dialogWidth), [**dialogTop**](/dom/WindowModal/dialogTop), and [**dialogLeft**](/dom/WindowModal/dialogLeft) properties. If the page (that contains this script) is hosted within an IFRAME, the IFRAME will move relative to the upper-left corner of the content area. Windows XP Service Pack 2 (SP2) or later. Windows that are located in the Internet Zone are subject to Window\_Restrictions and will be forced to stay on screen. This applies to [**moveTo**](/dom/Window/moveTo), [**moveBy**](/dom/Window/moveBy), **resizeTo**, and [**resizeBy**](/dom/Window/resizeBy) methods. **Note:** When operating in high-dpi mode, pixel values are scaled up accordingly. See Adjusting Scale for Higher DPI Screens for additional information. Windows Internet Explorer 7. This method is only effective when a single tab is open or when tabbed browsing is disabled. If multiple tabs are open, this method is blocked. For information regarding tab interaction from a script, see Tabbed Browsing for Developers. Internet Explorer 7. This method is blocked if called by a foreign domain within a sub-frame (FRAME/IFRAME).

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[resizeTo](https://developer.mozilla.org/en-US/docs/Web/API/Window.resizeTo) Article]

Portions of this content come from the Microsoft Developer Network: [[resizeTo Method](http://msdn.microsoft.com/en-us/library/ie/ms536723(v=vs.85).aspx) Article]

