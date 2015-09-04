---
title: remove
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Removes one or more tokens from a DOMTokenList.'
uri: dom/DOMTokenList/remove

---
# remove

## Summary

Removes one or more tokens from a DOMTokenList.

*Method of [dom/DOMTokenList](/dom/DOMTokenList)*

## Syntax

``` {.js}
var result = element.remove(token);
```

## Parameters

### token

 Data-typeÂ
:   String

 The token to remove from the DOMTokenList.

## Return Value

Returns an object of type Boolean.

## Examples

``` {.js}
//removes an item from an element's classList (a DOMTokenList)
function elRemItem(elid,itemrem) {
  var classes = document.getElementById(elid).classList;
  classes.remove(itemrem);
}
```

## Related specifications

Specification
:   Status
[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

