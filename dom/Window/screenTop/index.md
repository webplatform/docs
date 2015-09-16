---
title: 'screenTop'
attributions:
  - 'Microsoft Developer Network: [[screenTop Property](http://msdn.microsoft.com/en-us/library/ie/ms534390(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Window
standardization_status: Non-Standard
summary: 'Retrieves the y-coordinate of the top corner of the client area, relative to the top corner of the screen.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/screenTop

---
## Summary

Retrieves the y-coordinate of the top corner of the client area, relative to the top corner of the screen.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

**Note**: This property is read-only.

``` js
var top = window.screenTop;
```

## Return Value

Returns an object of type NumberNumber

the y-coordinate, in pixels.

## Examples

``` js
var top=window.screenTop;
```

## Notes

### Remarks

The client area consists of the window, exclusive of the caption bar, the window-sizing border, the menu bar, the toolbars, the scroll bars, and the status bars.

### Syntax
