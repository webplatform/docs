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
## Summary

Adds a token to a DOMTokenList if it is not present, or removes it if it is. Returns true if the token is now present (it was added); returns false if it is not (it was removed).

Method of [dom/DOMTokenList](/dom/DOMTokenList)[dom/DOMTokenList](/dom/DOMTokenList)

## Syntax

``` js
var tokenExists = tokenList.toggle(token, force);
```

## Parameters

### token

 Data-type
:   String

 The token to toggle.

### force

 Data-type
:   Boolean

(Optional)

Whether to force adding or removing the token. See Notes.

## Return Value

Returns an object of type BooleanBoolean

Whether the token exists after the method has executed.

## Examples

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

## Usage

     Throws a SyntaxError  exception if token is empty.

Throws an `InvalidCharacterError` exception if *token* contains any spaces.

## Notes

If the optional parameter *force* is not provided, this method removes the token if it is present, or adds the token if it is not present.

If *force* is *true*, this method adds the token (functionally equivalent to DOMTokenList.add()). If *force* is *false*, this method removes the token (functionally equivalent to DOMTokenList.remove()).

## Related specifications

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
