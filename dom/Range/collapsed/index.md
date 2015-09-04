---
title: collapsed
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The Range.collapsed read-only property returns a Boolean flag indicating whether the start and end points of the Range are at the same position. It returns true if the start and end boundary points of the Range are the same point in the DOM, false if not.'
uri: dom/Range/collapsed

---
# collapsed

## Summary

The Range.collapsed read-only property returns a Boolean flag indicating whether the start and end points of the Range are at the same position. It returns true if the start and end boundary points of the Range are the same point in the DOM, false if not.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Range](/dom/Range)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = range.collapsed;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

true - start and end boundary points of the Range are the same point in the DOM

false - start and end boundary points of the Range are NOT the same point in the DOM

## Examples

``` {.js}
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
var isCollapsed = range.collapsed;
```

## Notes

### Remarks

A collapsed range has its start and end boundary points set to the same value, rendering it empty.

### Syntax

isCollapsed = range.collapsed;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-collapsed)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.collapsed](https://developer.mozilla.org/en-US/docs/Web/API/Range.collapsed) Article]

Portions of this content come from the Microsoft Developer Network: [[collapsed Property](http://msdn.microsoft.com/en-us/library/ie/ff974925(v=vs.85).aspx) Article]

