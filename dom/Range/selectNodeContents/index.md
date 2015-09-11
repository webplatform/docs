---
title: selectNodeContents
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.selectNodeContents](https://developer.mozilla.org/en-US/docs/Web/API/Range.selectNodeContents) Article]'
  - 'Microsoft Developer Network: [[selectNodeContents Method](http://msdn.microsoft.com/en-us/library/ie/ff975447(v=vs.85).aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Range
    href: /dom/Range
  return_type:
    predicate: 'Returns an object of type  '
    value: Number
    href: /dom/Range
standardization_status: 'W3C Recommendation'
summary: 'Sets the Range to contain the contents of a Node.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/selectNodeContents

---
## <span>Summary</span>

Sets the Range to contain the contents of a Node.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## <span>Syntax</span>

``` js
var result = referenceNode.selectNodeContents(/* see parameter list */);
```

## <span>Parameters</span>

### <span>referenceNode</span>

 Data-type
:   DOM Node

 A node in the document hierarchy.

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|detach has been invoked on the object.|

## <span>Examples</span>

``` js
var range = document.createRange();
var referenceNode = document.getElementsByTagName("div")[0];
range.selectNodeContents(referenceNode);
```

### <span>Syntax</span>

range.selectNodeContents(referenceNode);

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[DOM](http://dom.spec.whatwg.org/#dom-range-selectnodecontents)
:   Living Standard
