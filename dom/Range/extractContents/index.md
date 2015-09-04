---
title: extractContents
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Recommendation'
summary: 'Removes the contents of a range from a document or document fragment and puts it a new document fragment.'
uri: dom/Range/extractContents

---
# extractContents

## Summary

Removes the contents of a range from a document or document fragment and puts it a new document fragment.

*Method of [dom/Range](/dom/Range)*

## Syntax

``` {.js}
var documentFragment = range.extractContents(/* see parameter list */);
```

## Parameters

### oDocumentFragment

 Data-typeÂ
:   any

 Returns an object that contains the extracted content.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
InvalidStateError
:   detach has been invoked on the object.
W3Exception\_DOM\_HIERARCHY\_REQUEST\_ERR
:   A document type node is included in the range that is being cloned.
W3Exception\_DOM\_NO\_MODIFICATION\_ALLOWED\_ERR
:   A node or portion of the content in the range is read-only.

## Examples

``` {.js}
range = document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
documentFragment = range.extractContents();
document.body.appendChild(documentFragment);
```

## Notes

Event Listeners added using DOM Events are not retained during extraction. HTML attribute events are retained or duplicated as they are for the Node.cloneNode() method. HTML id attributes are also cloned, which can lead to an invalid document if a partially-selected node is extracted and appened to the document.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## Related specifications

Specification
:   Status
[DOM](http://dom.spec.whatwg.org/#dom-range-extractcontents)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.extractContents](https://developer.mozilla.org/en-US/docs/Web/API/Range.extractContents) Article]

Portions of this content come from the Microsoft Developer Network: [[extractContents Method](http://msdn.microsoft.com/en-us/library/ie/ff975443(v=vs.85).aspx) Article]

