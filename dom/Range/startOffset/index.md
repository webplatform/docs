---
title: startOffset
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Retrieves the offset of the starting boundary point relative to the startContainer in the current range.'
uri: dom/Range/startOffset

---
# startOffset

## Summary

Retrieves the offset of the starting boundary point relative to the startContainer in the current range.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Range](/dom/Range)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var startRangeOffset = range.startOffset;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

the offset value.

## Examples

``` {.js}
var range = document.createRange();
range.setStart(startNode,startOffset);
range.setEnd(endNode,endOffset);
var startRangeOffset = range.startOffset;
```

## Notes

### Remarks

If the boundary point offset is within a container that is not a character data node, the offset is essentially a count based on where it falls between child nodes. For example, the offset is 0 if it falls before the first child and 1 if it is between the first and second child. If the offset is within a character data node container, the value represents 16-bit unit positions.

### Syntax

startRangeOffset = range.startOffset;

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-startoffset)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.startOffset](https://developer.mozilla.org/en-US/docs/Web/API/Range.startOffset) Article]

Portions of this content come from the Microsoft Developer Network: [[startOffset Property](http://msdn.microsoft.com/en-us/library/ie/ff974930(v=vs.85).aspx) Article]

