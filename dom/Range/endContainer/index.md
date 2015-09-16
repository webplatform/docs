---
title: 'endContainer'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.endContainer](https://developer.mozilla.org/en-US/docs/Web/API/Range.endContainer) Article]'
  - 'Microsoft Developer Network: [[endContainer Property](http://msdn.microsoft.com/en-us/library/ie/ff974927(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Range
    href: /dom/Range
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the end point node of the current range.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Range/endContainer

---
## Summary

Retrieves the end point node of the current range.

Property of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

**Note**: This property is read-only.

``` js
var endNode = range.endContainer;
```

## Return Value

Returns an object of type DOM NodeDOM Node

## Examples

``` js
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeNode = range.endContainer;
```

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-range-compareboundarypoints)
:   Living Standard
