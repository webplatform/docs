---
title: 'cloneContents'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.cloneContents](https://developer.mozilla.org/en-US/docs/Web/API/Range.cloneContents) Article]'
  - 'Microsoft Developer Network: [[cloneContents Method](http://msdn.microsoft.com/en-us/library/ie/ff975437(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Returns a document fragment containing the nodes of a range. If any nodes are partially selected, their start or end nodes are included.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/cloneContents

---
## Summary

Returns a document fragment containing the nodes of a range. If any nodes are partially selected, their start or end nodes are included.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var object = object.cloneContents(/* see parameter list */);
```

## Parameters

### oDocumentFragment

 Data-type
:   any

 Returns a document fragment object.

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|detach has been invoked on the object.|
|W3Exception\_DOM\_HIERARCHY\_REQUEST\_ERR|A document type node is included in the range that is being cloned.|

## Examples

``` js
var range = document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
var documentFragment = range.cloneContents();
document.body.appendChild(documentFragment);
```

### Syntax

documentFragment = range.cloneContents();

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13
