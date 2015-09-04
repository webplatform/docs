---
title: top
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
summary: 'Retrieves the topmost ancestor window.'
uri: dom/Window/top

---
# top

## Summary

Retrieves the topmost ancestor window.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Window](/dom/Window)</span></span>

## Syntax

``` {.js}
var topwindow = window.top;
window.top = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

## Examples

``` {.js}
var topwindow=window.top;
```

## Usage

     This property is especially useful when you are dealing with a window that is in a subframe of a parent or parents, and you want to get to the top-level frameset.

### Syntax

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[top](https://developer.mozilla.org/en-US/docs/Web/API/window.top) Article]

Portions of this content come from the Microsoft Developer Network: [[top Property](http://msdn.microsoft.com/en-us/library/ie/ms534687(v=vs.85).aspx) Article]

