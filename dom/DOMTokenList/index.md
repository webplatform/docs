---
title: DOMTokenList
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: "Represents a space-separated token list within the DOM, such as the contents of the className property of an element, treated as a zero-based array-like object.\nDOMTokenList objects are case-sensitive, even when the underlying string might ordinarily be treated in a case-insensitive manner.\n"
tags:
  - API
  - Objects
  - DOM
uri: dom/DOMTokenList

---
## Summary

Represents a space-separated token list within the DOM, such as the contents of the className property of an element, treated as a zero-based array-like object. DOMTokenList objects are case-sensitive, even when the underlying string might ordinarily be treated in a case-insensitive manner.

## Properties

API Name
:   Summary

[length](/dom/DOMTokenList/length)
:   Returns the number of tokens in a DOMTokenList.

## Methods

API Name
:   Summary

[add](/dom/DOMTokenList/add)
:   Adds one or more tokens to a DOMTokenList.

[contains](/dom/DOMTokenList/contains)
:   Tests if a token is part of a DOMTokenList.

[remove](/dom/DOMTokenList/remove)
:   Removes one or more tokens from a DOMTokenList.

[toggle](/dom/DOMTokenList/toggle)
:   Adds a token to a DOMTokenList if it is not present, or removes it if it is. Returns `true` if the token is now present (it was added); returns `false` if it is not (it was removed).

[item](/dom/DomTokenList/item)
:   Returns a specific zero-indexed token from a DOMTokenList.

## Events

*No events.*

## Notes

A DOMTokenList object will stringify to the value of the DOMTokenList object's underlying string. A set of space-separated tokens is a string containing zero or more words (known as tokens) separated by one or more space characters, where words consist of any string of one or more characters, none of which are space characters (the space characters are U+0020 SPACE, U+0009 CHARACTER TABULATION (tab), U+000A LINE FEED (LF), U+000C FORM FEED (FF), and U+000D CARRIAGE RETURN (CR)).

## Related specifications

[W3C DOM4](http://www.w3.org/TR/dom/)
:   Candidate Recommendation
