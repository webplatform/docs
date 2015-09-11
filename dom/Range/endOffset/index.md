---
title: endOffset
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
  - API
  - Object
  - Properties
  - DOM
uri: dom/Range/endOffset

---
## <span>Summary</span>

Returns a number representing where in the Range.endContainer the Range ends.

Property of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var offset = range.endOffset;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

the end offset value.

## <span>Examples</span>

``` js
var range = document.createRange();

range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
endRangeOffset = range.endOffset;
```

## <span>Notes</span>

### <span>Remarks</span>

If the boundary point offset is within a container that is not a character data node, the offset is a count based on where it falls between child nodes. For example, the offset is 0 if it falls before the first child, and 1 if it is between the first and second child. If the offset is within a character data node container, the value represents 16-bit unit positions.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[DOM](http://dom.spec.whatwg.org/#dom-range-endoffset)
:   Living Standard
