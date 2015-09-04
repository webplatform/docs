---
title: length
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Returns the number of tokens in a DOMTokenList.'
uri: dom/DOMTokenList/length

---
# length

## Summary

Returns the number of tokens in a DOMTokenList.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/DOMTokenList](/dom/DOMTokenList)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = element.length;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Number</span></span>

## Examples

``` {.js}
//returns the number of classes in an element's classList (a DOMTokenList)
function elNumClasses(elid) {
  var classes = document.getElementById(elid).classList;
  return classes.length;
}
```

## Related specifications

Specification
:   Status
[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

