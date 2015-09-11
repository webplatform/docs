---
title: contains
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
## <span>Summary</span>

Tests if a token is part of a DOMTokenList.

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

``` js
var tokenExists = tokenList.contains(token);
```

## <span>Parameters</span>

### <span>token</span>

 Data-type
:   String

 The requested token.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the given token exists in the list. Returns `true` if the token is present; `false` otherwise.

## <span>Examples</span>

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

## <span>Notes</span>

Throws a `SyntaxError` exception if *token* is empty.

Throws an `InvalidCharacterError` exception if *token* contains any spaces.

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `DOMTokenList`
