---
title: selectNode
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Selects a range node and all of its contents.'
uri: dom/Range/selectNode

---
# selectNode

## Summary

Selects a range node and all of its contents.

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var result = range.selectNode(/* see parameter list */);
```

## Parameters

### referenceNode

 Data-typeÂ
:   DOM Node

 The node to select.

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

range.selectNode(referenceNode);
```

### Syntax

range.selectNode(referenceNode);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-selectnode)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.selectNode](https://developer.mozilla.org/en-US/docs/Web/API/Range.selectNode) Article]

Portions of this content come from the Microsoft Developer Network: [[selectNode Method](http://msdn.microsoft.com/en-us/library/ie/ff975446(v=vs.85).aspx) Article]

