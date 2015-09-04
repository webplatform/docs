---
title: contains
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Tests if a token is part of a DOMTokenList.'
uri: dom/DOMTokenList/contains

---
# contains

## Summary

Tests if a token is part of a DOMTokenList.

*Method of [dom/DOMTokenList](/dom/DOMTokenList)*

## Syntax

``` {.js}
var tokenExists = tokenList.contains(token);
```

## Parameters

### token

 Data-typeÂ
:   String

 The requested token.

## Return Value

Returns an object of type Boolean.

Whether the given token exists in the list. Returns `true` if the token is present; `false` otherwise.

## Examples

``` {.js}
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

Specification
:   Status
[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

## See also

### Related pages (MSDN)

-   `DOMTokenList`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

