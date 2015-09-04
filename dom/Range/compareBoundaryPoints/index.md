---
title: compareBoundaryPoints
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.'
uri: dom/Range/compareBoundaryPoints

---
# compareBoundaryPoints

## Summary

The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var boundaryComparison = range.compareBoundaryPoints(/* see parameter list */);
```

## Parameters

### how

 Data-typeÂ
:   unsigned short

 Specifies how *sourceRange* is compared to the range of the object on which **compareBoundaryPoints** is invoked.

Must be one of -

\`Range.END\_TO\_END\` (2) compares the end boundary-point of sourceRange to the end boundary-point of Range.

\`Range.END\_TO\_START\` (3) compares the end boundary-point of sourceRange to the start boundary-point of Range.

\`Range.START\_TO\_END\` (1) compares the start boundary-point of sourceRange to the end boundary-point of Range.

\`Range.START\_TO\_START\` (0) compares the start boundary-point of sourceRange to the start boundary-point of Range.

### sourceRange

 Data-typeÂ
:   Range

[**Range**](/dom/Range) objectÂ that is compared to the range of the object on which **compareBoundaryPoints** is invoked.

## Return Value

Returns an object of type Number.

Returns a â€“1, 0, or 1 to indicate whether the *sourceRange* point is before, equal to, or after the boundary point of the [**Range**](/dom/Range) object on which **compareBoundaryPoints** is invoked.

## Examples

``` {.js}
var range, sourceRange, compare;
range = document.createRange();
range.selectNode(document.getElementsByTagName("div")[0]);
sourceRange = document.createRange();
sourceRange.selectNode(document.getElementsByTagName("div")[1]);
compare = range.compareBoundaryPoints(Range.START_TO_END, sourceRange);
```

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-compareboundarypoints)
:   Living Standard
[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level-2-Range-Comparing)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.compareBoundaryPoints](https://developer.mozilla.org/en-US/docs/Web/API/Range.compareBoundaryPoints) Article]

Portions of this content come from the Microsoft Developer Network: [[compareBoundaryPoints Method](http://msdn.microsoft.com/en-us/library/ie/ff975440(v=vs.85).aspx) Article]

