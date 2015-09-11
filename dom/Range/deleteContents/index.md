---
title: deleteContents
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.deleteContents](https://developer.mozilla.org/en-US/docs/Web/API/Range.deleteContents) Article]'
  - 'Microsoft Developer Network: [[deleteContents Method](http://msdn.microsoft.com/en-us/library/ie/ff975441(v=vs.85).aspx) Article]'
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
summary: 'Removes all contents within a selected range.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/deleteContents

---
## <span>Summary</span>

Removes all contents within a selected range.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## <span>Syntax</span>

``` js
var object = object.deleteContents();
```

## <span>Return Value</span>

Returns an object of type NumberNumber

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|detach has been invoked on the object.|
|W3Exception\_DOM\_NO\_MODIFICATION\_ALLOWED\_ERR|Some of the contents or nodes are read-only.|

## <span>Examples</span>

``` js
var range = document.createRange();
range.selectNode(document.getElementsByTagName("div").item(0));
range.deleteContents();
```

## <span>Notes</span>

### <span>Remarks</span>

If the deleted range contains closing or opening tags, the remaining tags are completed.

### <span>Syntax</span>

Range.deleteContents();

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13

## <span>Related specifications</span>

[DOM](http://dom.spec.whatwg.org/#dom-range-deletecontents)
:   Living Standard
