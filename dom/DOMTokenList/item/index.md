---
title: 'item'
compatibility:
  feature: item
  topic: dom
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/DOMTokenList
    href: /dom/DOMTokenList
  return_type:
    predicate: 'Returns an object of type  '
    value: String
    href: /dom/DOMTokenList
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns a specific zero-indexed token from a DOMTokenList.'
tags:
  - API_Object_Methods
  - DOM
uri: dom/DomTokenList/item

---
## Summary

Returns a specific zero-indexed token from a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## Syntax

``` js
var result = element.item(index);
```

## Parameters

### index

 Data-type
:   Number

 The index of the token to retrieve.

## Return Value

Returns an object of type StringString

## Examples

``` js
//returns a specific item from an element's classList (a DOMTokenList)
function elItem(elid,num) {
  var classes = document.getElementById(elid).classList;
  return classes.item(num);
}
```

## Usage

     DOMTokenList.item(n) is functionally equivalent to DOMTokenList[n] in that it references an indexed item in the DOMTokenList.

## Related specifications

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
