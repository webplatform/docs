---
title: toggle
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
standardization_status: 'W3C Working Draft'
summary: 'Adds a token to a DOMTokenList if it is not present, or removes it if it is. Returns true if the token is now present (it was added); returns false if it is not (it was removed).'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/DOMTokenList/toggle

---
## <span>Summary</span>

Adds a token to a DOMTokenList if it is not present, or removes it if it is. Returns true if the token is now present (it was added); returns false if it is not (it was removed).

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## <span>Syntax</span>

``` js
var tokenExists = tokenList.toggle(token, force);
```

## <span>Parameters</span>

### <span>token</span>

 Data-type
:   String

 The token to toggle.

### <span>force</span>

 Data-type
:   Boolean

(Optional)

Whether to force adding or removing the token. See Notes.

## <span>Return Value</span>

Returns an object of type BooleanBoolean

Whether the token exists after the method has executed.

## <span>Examples</span>

``` js
//toggles an item in an element's classList (a DOMTokenList)
//the item will be added if it does not exist, or removed if it does exist
function elTogItem(elid,itemtog) {
  var classes = document.getElementById(elid).classList;
  return classes.toggle(itemtog);
}
```

``` js
//toggles an item in an element's classList (a DOMTokenList)
//the item will be added if force is true, or removed if force is false,
//functionally equivalent to .add() and .remove(), respectively
function elTogItemForce(elid,itemtog,force) {
  var classes = document.getElementById(elid).classList;
  return classes.toggle(itemtog,force);
}
```

## <span>Usage</span>

     Throws a SyntaxError  exception if token is empty.

Throws an `InvalidCharacterError` exception if *token* contains any spaces.

## <span>Notes</span>

If the optional parameter *force* is not provided, this method removes the token if it is present, or adds the token if it is not present.

If *force* is *true*, this method adds the token (functionally equivalent to DOMTokenList.add()). If *force* is *false*, this method removes the token (functionally equivalent to DOMTokenList.remove()).

## <span>Related specifications</span>

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
