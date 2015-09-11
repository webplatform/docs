---
title: add
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
summary: 'Adds one or more tokens to a DOMTokenList.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DOMTokenList/add

---
## <span>Summary</span>

Adds one or more tokens to a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

``` js
var result = element.add(token);
```

## <span>Parameters</span>

### <span>token</span>

 Data-type
:   String

 The token to add to the DOMTokenList.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

## <span>Examples</span>

``` js
//adds an item to an element's classList (a DOMTokenList)
function elAddItem(elid,itemadd) {
  var classes = document.getElementById(elid).classList;
  classes.add(itemadd);
}
```

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
