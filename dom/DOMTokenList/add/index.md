---
title: add
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Adds one or more tokens to a DOMTokenList.'
uri: dom/DOMTokenList/add

---
# add

## Summary

Adds one or more tokens to a DOMTokenList.

*Method of [dom/DOMTokenList](/dom/DOMTokenList)*

## Syntax

``` {.js}
var result = element.add(token);
```

## Parameters

### token

 Data-typeÂ
:   String

 The token to add to the DOMTokenList.

## Return Value

Returns an object of type Boolean.

## Examples

``` {.js}
//adds an item to an element's classList (a DOMTokenList)
function elAddItem(elid,itemadd) {
  var classes = document.getElementById(elid).classList;
  classes.add(itemadd);
}
```

## Related specifications

Specification
:   Status
[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

