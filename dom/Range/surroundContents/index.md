---
title: surroundContents
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Moves the contents of a Range to a new parent node, placing the new parent node at the start position of the Range.'
uri: dom/Range/surroundContents

---
# surroundContents

## Summary

Moves the contents of a Range to a new parent node, placing the new parent node at the start position of the Range.

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var result = range.surroundContents(/* see parameter list */);
```

## Parameters

### newNode

 Data-typeÂ
:   DOM Node

 The new node to make the parent.

## Return Value

Returns an object of type Number.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
HierarchyRequestError
:   A document type node is included in the Range that is being cloned.
InvalidStateError
:   detach has been invoked on the object.
NoModificationAllowedError
:   A boundary point in the Range is read-only.

## Examples

``` {.js}
var range = document.createRange();
var newNode = document.createElement("p");

range.selectNode(document.getElementsByTagName("div").item(0));
range.surroundContents(newNode);
```

## Notes

### Remarks

If the *newParent* already exists in the document, its content is removed.

### Syntax

range.surroundContents(newNode);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-surroundcontents)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.surroundContents](https://developer.mozilla.org/en-US/docs/Web/API/Range.surroundContents) Article]

Portions of this content come from the Microsoft Developer Network: [[surroundContents Method](http://msdn.microsoft.com/en-us/library/ie/ff975454(v=vs.85).aspx) Article]

