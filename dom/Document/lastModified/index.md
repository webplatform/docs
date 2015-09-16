---
title: 'lastModified'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs examples and compat tables'
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
summary: 'Gets the date that the document was last modified, if the document supplies one.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/lastModified

---
## Summary

Gets the date that the document was last modified, if the document supplies one.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var lastModified = document.lastModified;
```

## Return Value

Returns an object of type StringString

The date of the last modification to the document, as indicated by the server.

**Needs Examples**: This section should include examples.

## Related specifications

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
