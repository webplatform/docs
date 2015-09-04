---
title: item
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs compat table'
summary: 'Returns a specific zero-indexed token from a DOMTokenList.'
uri: dom/DomTokenList/item

---
# item

## Summary

Returns a specific zero-indexed token from a DOMTokenList.

*Method of [dom/DOMTokenList](/dom/DOMTokenList)*

## Syntax

``` {.js}
var result = element.item(index);
```

## Parameters

### index

 Data-typeÂ
:   Number

 The index of the token to retrieve.

## Return Value

Returns an object of type String.

## Examples

``` {.js}
//returns a specific item from an element's classList (a DOMTokenList)
function elItem(elid,num) {
  var classes = document.getElementById(elid).classList;
  return classes.item(num);
}
```

## Usage

     DOMTokenList.item(n) is functionally equivalent to DOMTokenList[n] in that it references an indexed item in the DOMTokenList.

## Related specifications

Specification
:   Status
[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

