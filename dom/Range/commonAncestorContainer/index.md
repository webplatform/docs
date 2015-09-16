---
title: 'commonAncestorContainer'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.commonAncestorContainer](https://developer.mozilla.org/en-US/docs/Web/API/Range.commonAncestorContainer) Article]'
  - 'Microsoft Developer Network: [[commonAncestorContainer Property](http://msdn.microsoft.com/en-us/library/ie/ff974926(v=vs.85).aspx) Article]'
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
summary: 'Returns the deepest node in which two boundary points exist.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Range/commonAncestorContainer

---
## Summary

Returns the deepest node in which two boundary points exist.

Property of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

**Note**: This property is read-only.

``` js
var rangeAcestor = range.commonAncestorContainer;
```

## Return Value

Returns an object of type DOM NodeDOM Node

Node that contains both the Range.startContainer and Range.endContainer nodes.

## Examples

``` js
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

[DOM](http://dom.spec.whatwg.org/#dom-range-commonancestorcontainer)
:   Living Standard
