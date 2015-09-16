---
title: top
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[top](https://developer.mozilla.org/en-US/docs/Web/API/window.top) Article]'
  - 'Microsoft Developer Network: [[top Property](http://msdn.microsoft.com/en-us/library/ie/ms534687(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Window
    href: /dom/Window
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Window
summary: 'Retrieves the topmost ancestor window.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Window/top

---
## Summary

Retrieves the topmost ancestor window.

Property of [dom/Window](/dom/Window)[dom/Window](/dom/Window)

## Syntax

``` js
var topwindow = window.top;
window.top = value;
```

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

``` js
var topwindow=window.top;
```

## Usage

     This property is especially useful when you are dealing with a window that is in a subframe of a parent or parents, and you want to get to the top-level frameset.

### Syntax
