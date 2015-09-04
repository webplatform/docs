---
title: startContainer
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the starting node of a current range'
uri: dom/Range/startContainer

---
# startContainer

## Summary

Retrieves the starting node of a current range

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Range](/dom/Range)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var startRangeNode = range.startContainer;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The starting node in the range

## Examples

``` {.js}
var range = document.createRange();
range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
var startRangeNode = range.startContainer;
```

### Syntax

startRangeNode = range.startContainer;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-startcontainer)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.startContainer](https://developer.mozilla.org/en-US/docs/Web/API/Range.startContainer) Article]

Portions of this content come from the Microsoft Developer Network: [[startContainer Property](http://msdn.microsoft.com/en-us/library/ie/ff974929(v=vs.85).aspx) Article]

