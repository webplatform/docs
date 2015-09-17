---
title: 'parentElement'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples, spec, and compat'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
summary: 'Retrieves the parent node of this DOM node, if the parent is an element node; null if the parent is not an element or if there is no parent.  Read-only.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/Element/parentElement

---
## Summary

Retrieves the parent node of this DOM node, if the parent is an element node; null if the parent is not an element or if there is no parent. Read-only.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

**Note**: This property is read-only.

``` js
var result = element.parentElement;
```

## Notes

### Remarks

The topmost object returns `null` as its parent.

### Syntax
