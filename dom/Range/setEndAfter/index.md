---
title: setEndAfter
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Sets the end of a range to a point after a specific node.'
uri: dom/Range/setEndAfter

---
# setEndAfter

## Summary

Sets the end of a range to a point after a specific node.

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var result = range.setEndAfter(/* see parameter list */);
```

## Parameters

### referenceNode

 Data-typeÂ
:   DOM Node

 A node in the document hierarchy.

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

## Examples

``` {.js}
var range = document.createRange();
var referenceNode = document.getElementsByTagName("div").item(0);

range.setEndAfter(referenceNode);
```

### Syntax

range.setEndAfter(referenceNode);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-setendafter)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.setEndAfter](https://developer.mozilla.org/en-US/docs/Web/API/Range.setEndAfter) Article]

Portions of this content come from the Microsoft Developer Network: [[setEndAfter Method](http://msdn.microsoft.com/en-us/library/ie/ff975449(v=vs.85).aspx) Article]

