---
title: screenLeft
attributions:
  - 'Microsoft Developer Network: [[screenLeft Property](http://msdn.microsoft.com/en-us/library/ie/ms534389(v=vs.85).aspx) Article]'
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
summary: 'Retrieves the x-coordinate of the upper left-hand corner of the window frame, relative to the upper left-hand corner of the screen. '
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/screenLeft

---
## <span>Summary</span>

Retrieves the x-coordinate of the upper left-hand corner of the window frame, relative to the upper left-hand corner of the screen.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = window.screenLeft;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

the x-coordinate, in pixels.

## <span>Examples</span>

``` js
var left=window.screenLeft;
```

## <span>Notes</span>

### <span>Remarks</span>

The client area consists of the frame area, exclusive of the caption bar, the window-sizing border, the menu bar, the toolbars, the scroll bars, and the status bars.

### <span>Syntax</span>