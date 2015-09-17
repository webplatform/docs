---
title: 'compareBoundaryPoints'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.compareBoundaryPoints](https://developer.mozilla.org/en-US/docs/Web/API/Range.compareBoundaryPoints) Article]'
  - 'Microsoft Developer Network: [[compareBoundaryPoints Method](http://msdn.microsoft.com/en-us/library/ie/ff975440(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Range/compareBoundaryPoints

---
## Summary

The Range.compareBoundaryPoints() method compares the boundary points of the Range with another one.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var boundaryComparison = range.compareBoundaryPoints(/* see parameter list */);
```

## Parameters

### how

 Data-type
:   unsigned short

 Specifies how *sourceRange* is compared to the range of the object on which **compareBoundaryPoints** is invoked.

Must be one of -

\`Range.END\_TO\_END\` (2) compares the end boundary-point of sourceRange to the end boundary-point of Range.

\`Range.END\_TO\_START\` (3) compares the end boundary-point of sourceRange to the start boundary-point of Range.

\`Range.START\_TO\_END\` (1) compares the start boundary-point of sourceRange to the end boundary-point of Range.

\`Range.START\_TO\_START\` (0) compares the start boundary-point of sourceRange to the start boundary-point of Range.

### sourceRange

 Data-type
:   Range

[**Range**](/dom/Range) object that is compared to the range of the object on which **compareBoundaryPoints** is invoked.

## Return Value

Returns an object of type NumberNumber

Returns a –1, 0, or 1 to indicate whether the *sourceRange* point is before, equal to, or after the boundary point of the [**Range**](/dom/Range) object on which **compareBoundaryPoints** is invoked.

## Examples

``` js
var range, sourceRange, compare;
range = document.createRange();
range.selectNode(document.getElementsByTagName("div")[0]);
sourceRange = document.createRange();
sourceRange.selectNode(document.getElementsByTagName("div")[1]);
compare = range.compareBoundaryPoints(Range.START_TO_END, sourceRange);
```

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-range-compareboundarypoints)
:   Living Standard

[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level-2-Range-Comparing)
:   Recommendation
