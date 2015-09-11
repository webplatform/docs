---
title: item
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
  - API
  - Object
  - Methods
  - DOM
uri: dom/DomTokenList/item

---
## <span>Summary</span>

Returns a specific zero-indexed token from a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

``` js
var result = element.item(index);
```

## <span>Parameters</span>

### <span>index</span>

 Data-type
:   Number

 The index of the token to retrieve.

## <span>Return Value</span>

Returns an object of type StringString

## <span>Examples</span>

``` js
//returns a specific item from an element's classList (a DOMTokenList)
function elItem(elid,num) {
  var classes = document.getElementById(elid).classList;
  return classes.item(num);
}
```

## <span>Usage</span>

     DOMTokenList.item(n) is functionally equivalent to DOMTokenList[n] in that it references an indexed item in the DOMTokenList.

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
