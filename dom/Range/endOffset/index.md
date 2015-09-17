---
title: 'endOffset'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.endOffset](https://developer.mozilla.org/en-US/docs/Web/API/Range.endOffset) Article]'
  - 'Microsoft Developer Network: [[endOffset Property](http://msdn.microsoft.com/en-us/library/ie/ff974928(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Range
    href: /dom/Range
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Returns a number representing where in the Range.endContainer the Range ends.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Range/endOffset

---
## Summary

Returns a number representing where in the Range.endContainer the Range ends.

Property of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

**Note**: This property is read-only.

``` js
var offset = range.endOffset;
```

## Return Value

Returns an object of type NumberNumber

the end offset value.

## Examples

``` js
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeOffset = range.endOffset;
```

## Notes

### Remarks

If the boundary point offset is within a container that is not a character data node, the offset is a count based on where it falls between child nodes. For example, the offset is 0 if it falls before the first child, and 1 if it is between the first and second child. If the offset is within a character data node container, the value represents 16-bit unit positions.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

[DOM](http://dom.spec.whatwg.org/#dom-range-endoffset)
:   Living Standard
