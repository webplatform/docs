---
title: 'setStartBefore'
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [[Range.setStartBefore](https://developer.mozilla.org/en-US/docs/Web/API/Range.setStartBefore) Article]'
  - 'Microsoft Developer Network: [[setStartBefore Method](http://msdn.microsoft.com/en-us/library/ie/ff975453(v=vs.85).aspx) Article]'
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
summary: 'Sets the start point of a range to a point before a specific node.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/Range/setStartBefore

---
## Summary

Sets the start point of a range to a point before a specific node.

Method of [dom/Range](/dom/Range)[dom/Range](/dom/Range)

## Syntax

``` js
var result = range.setStartBefore(/* see parameter list */);
```

## Parameters

### referenceNode

 Data-type
:   DOM Node

 Node in the document hierarchy.

## Return Value

Returns an object of type NumberNumber

Type: **HRESULT**

This method can return one of these values.

|Return code|Description|
|:----------|:----------|
|S\_OK|The operation completed successfully.|
|InvalidStateError|detach has been invoked on the object.|

## Examples

``` js
var range = document.createRange();
var referenceNode = document.getElementsByTagName("div").item(0);

range.setStartBefore(referenceNode);
```

### Syntax

range.setStartBefore(referenceNode);

### Standards information

-   [Document Object Model (DOM) Level 2 Traversal and Range Specification](http://go.microsoft.com/fwlink/p/?linkid=182712), Section 2.13
