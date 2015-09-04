---
title: endContainer
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the end point node of the current range.'
uri: dom/Range/endContainer

---
# endContainer

## Summary

Retrieves the end point node of the current range.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Range](/dom/Range)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var endNode = range.endContainer;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

## Examples

``` {.js}
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeNode = range.endContainer;
```

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-compareboundarypoints)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.endContainer](https://developer.mozilla.org/en-US/docs/Web/API/Range.endContainer) Article]

Portions of this content come from the Microsoft Developer Network: [[endContainer Property](http://msdn.microsoft.com/en-us/library/ie/ff974927(v=vs.85).aspx) Article]

