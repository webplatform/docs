---
title: 'readyState'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /dom/Document
standardization_status: 'W3C Working Draft'
summary: 'Retrieves a value that indicates the current state of the object.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Document/readyState

---
## Summary

Retrieves a value that indicates the current state of the object.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var readyState = node.readyState;
```

## Return Value

Returns an object of type StringString

## Usage

     The states through which an object passes are determined by that object; an object can skip certain states (for example, interactive) if those states do not apply to that object.

## Related specifications

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
