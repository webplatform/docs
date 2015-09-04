---
title: setStart
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the starting point of a range'
uri: dom/Range/setStart

---
# setStart

## Summary

Sets the starting point of a range

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var result = range.setStart(/* see parameter list */);
```

## Parameters

### startNode

 Data-typeÂ
:   DOM Node

 Node in the document hierarchy.

### startOffset

 Data-typeÂ
:   Number

 Specifies the offset value for the starting point.

## Return Value

Returns an object of type Number.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
InvalidStateError
:   detach has been invoked on the object.
W3Exception\_DOM\_INDEX\_SIZE\_ERR
:   offset is negative or greater than the number of child units in refNode.

Â

## Examples

``` {.js}
var range = document.createRange();
var startNode = document.getElementsByTagName("p").item(2);
var startOffset = 0;
range.setStart(startNode,startOffset);
```

## Notes

If the startNode is a Node of type Text, Comment, or CDATASection, then startOffset is the number of characters from the start of startNode. For other Node types, startOffset is the number of child nodes between the start of the startNode.

### Syntax

range.setStart(startNode, startOffset);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-setstart)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.setStart](https://developer.mozilla.org/en-US/docs/Web/API/Range.setStart) Article]

Portions of this content come from the Microsoft Developer Network: [[setStart Method](http://msdn.microsoft.com/en-us/library/ie/ff975451(v=vs.85).aspx) Article]

