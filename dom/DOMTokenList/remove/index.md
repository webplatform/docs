---
title: remove
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
## <span>Summary</span>

Removes one or more tokens from a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

``` js
var result = element.remove(token);
```

## <span>Parameters</span>

### <span>token</span>

 Data-type
:   String

 The token to remove from the DOMTokenList.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

``` js
//removes an item from an element's classList (a DOMTokenList)
function elRemItem(elid,itemrem) {
  var classes = document.getElementById(elid).classList;
  classes.remove(itemrem);
}
```

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
