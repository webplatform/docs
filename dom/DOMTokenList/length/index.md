---
title: length
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/DOMTokenList
    href: /dom/DOMTokenList
  return:
    predicate: 'Returns an object of type '
    value: Number
    href: /dom/DOMTokenList
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns the number of tokens in a DOMTokenList.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/DOMTokenList/length

---
## <span>Summary</span>

Returns the number of tokens in a DOMTokenList.

Property of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = element.length;
```

## <span>Return Value</span>

Returns an object of type NumberNumber

## <span>Examples</span>

``` js
//returns the number of classes in an element's classList (a DOMTokenList)
function elNumClasses(elid) {
  var classes = document.getElementById(elid).classList;
  return classes.length;
}
```

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
