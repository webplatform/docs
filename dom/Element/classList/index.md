---
title: classList
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples, compat, better spec link'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /dom/Element
standardization_status: 'W3C Candidate Recommendation'
summary: 'Reflects the class attribute as an ordered list of the whitespace separated class names and has convenience methods for add, remove, contains and more.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Element/classList

---
## Summary

Reflects the class attribute as an ordered list of the whitespace separated class names and has convenience methods for add, remove, contains and more.

Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

**Note**: This property is read-only.

``` js
var classList = element.classList;
```

## Return Value

Returns an object of type

A DOMTokenList representing the class names of the element.

**Needs Examples**: This section should include examples.

## Related specifications

[WHATWG DOM](http://dom.spec.whatwg.org/)
:   Living Standard

[DOM4](http://www.w3.org/TR/dom/)
:   Working Draft

## See also

### Related pages (MSDN)

-   `HTMLElement`
