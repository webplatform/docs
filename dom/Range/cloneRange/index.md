---
title: 'cloneRange'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.cloneRange](https://developer.mozilla.org/en-US/docs/Web/API/Range.cloneRange) Article]'
  - 'Microsoft Developer Network: [[cloneRange Method](http://msdn.microsoft.com/en-us/library/ie/ff975438(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: Range
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Returns a new range with boundary points that are equal to the original range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/cloneRange

---
## Summary

Returns a new range with boundary points that are equal to the original range.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var clone = range.cloneRange();
```

## Return Value

Returns an object of type RangeRange

## Examples

``` js
var range = document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
var clone = range.cloneRange();
```

### Syntax

clone = range.cloneRange();

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13
