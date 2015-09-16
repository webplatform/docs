---
title: 'contains'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
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
summary: 'Tests if a token is part of a DOMTokenList.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DOMTokenList/contains

---
## Summary

Tests if a token is part of a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## Syntax

``` js
var tokenExists = tokenList.contains(token);
```

## Parameters

### token

 Data-type
:   String

 The requested token.

## Return Value

Returns an object of type BooleanBoolean

Whether the given token exists in the list. Returns `true` if the token is present; `false` otherwise.

## Examples

``` js
// check an element's classList (a DOMTokenList) for a specific class
function elHasClass(elid, cls) {
  var classes = document.getElementById(elid).classList;
  if (classes.contains(cls))
    return true;
  else
    return false;
}
```

## Notes

Throws a `SyntaxError` exception if *token* is empty.

Throws an `InvalidCharacterError` exception if *token* contains any spaces.

## Related specifications

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

## See also

### Related pages

-   DOMTokenList[DOMTokenList](/dom/DOMTokenList)
