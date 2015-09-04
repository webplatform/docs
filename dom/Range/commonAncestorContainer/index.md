---
title: commonAncestorContainer
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Returns the deepest node in which two boundary points exist.'
uri: dom/Range/commonAncestorContainer

---
# commonAncestorContainer

## Summary

Returns the deepest node in which two boundary points exist.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Range](/dom/Range)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var rangeAcestor = range.commonAncestorContainer;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

Node that contains both the Range.startContainer and Range.endContainer nodes.

## Examples

``` {.js}
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
rangeAncestor = range.commonAncestorContainer;
```

### Syntax

rangeAncestor = range.commonAncestorContainer;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-commonancestorcontainer)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.commonAncestorContainer](https://developer.mozilla.org/en-US/docs/Web/API/Range.commonAncestorContainer) Article]

Portions of this content come from the Microsoft Developer Network: [[commonAncestorContainer Property](http://msdn.microsoft.com/en-us/library/ie/ff974926(v=vs.85).aspx) Article]

