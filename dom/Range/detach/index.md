---
title: detach
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.detatch](https://developer.mozilla.org/en-US/docs/Web/API/Range.detach) Article]'
  - 'Microsoft Developer Network: [[detatch Method](http://msdn.microsoft.com/en-us/library/ie/ff975442(v=vs.85).aspx) Article]'
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
summary: 'Removes or detaches a Range object and associated resources form a document.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Range/detach

---
## Summary

Removes or detaches a Range object and associated resources form a document.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var result = range.detach();
```

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|If detach has been invoked on the object.|

## Examples

``` js
var range = document.createRange();

range.selectNode(document.getElementsByTagName("div").item(0));
range.detach();
```

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13
