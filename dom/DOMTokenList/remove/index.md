---
title: 'remove'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DOMTokenList
    href: /dom/DOMTokenList
  return_type:
    predicate: 'Returns an object of type  '
    value: Boolean
    href: /dom/DOMTokenList
standardization_status: 'W3C Candidate Recommendation'
summary: 'Removes one or more tokens from a DOMTokenList.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DOMTokenList/remove

---
## Summary

Removes one or more tokens from a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## Syntax

``` js
var result = element.remove(token);
```

## Parameters

### token

 Data-type
:   String

 The token to remove from the DOMTokenList.

## Return Value

Returns an object of type BooleanBoolean

## Examples

``` js
//removes an item from an element's classList (a DOMTokenList)
function elRemItem(elid,itemrem) {
  var classes = document.getElementById(elid).classList;
  classes.remove(itemrem);
}
```

## Related specifications

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
