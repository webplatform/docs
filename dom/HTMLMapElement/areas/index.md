---
title: 'areas'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLMapElement
    href: /dom/HTMLMapElement
  return:
    predicate: 'Returns an object of type '
    value: Object
    href: /dom/HTMLMapElement
standardization_status: 'W3C Recommendation'
summary: 'Returns an HTMLCollection of area elements included within the element.'
tags:
  - API_Object_Properties
  - DOM
  - Needs_Examples
uri: dom/HTMLMapElement/areas

---
## Summary

Returns an HTMLCollection of area elements included within the element.

Property of [dom/HTMLMapElement](/dom/HTMLMapElement)[dom/HTMLMapElement](/dom/HTMLMapElement)

## Syntax

**Note**: This property is read-only.

``` js
var areaElements = mapElement.areas;
```

## Return Value

Returns an object of type ObjectObject

An HTMLCollection of [area](/dom/HTMLAreaElement) elements.

## Notes

Areas can be added to or removed from the collection. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position. To add elements to the collection, use the [**createElement**](/dom/Document/createElement) and [**add**](/dom/HTMLSelectElement/add) methods. Alternatively, use the [**insertAdjacentHTML**](/dom/Element/insertAdjacentHTML) method.

## Related specifications

[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation
