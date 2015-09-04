---
title: areas
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'examples, compatibility'
summary: 'Returns an HTMLCollection of area elements included within the element.'
uri: dom/HTMLMapElement/areas

---
# areas

## Summary

Returns an HTMLCollection of area elements included within the element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLMapElement](/dom/HTMLMapElement)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var areaElements = mapElement.areas;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Object</span></span>

An HTMLCollection of [area](/dom/HTMLAreaElement) elements.

**Needs Examples**: This section should include examples.

## Notes

Areas can be added to or removed from the collection. If duplicate identifiers are found, a collection of those items is returned. Collections of duplicates must be referenced subsequently by ordinal position. To add elements to the collection, use the [**createElement**](/dom/Document/createElement) and [**add**](/dom/HTMLSelectElement/add) methods. Alternatively, use the [**insertAdjacentHTML**](/dom/Element/insertAdjacentHTML) method.

## Related specifications

Specification
:   Status
[DOM Level 2 HTML](http://www.w3.org/TR/DOM-Level-2-HTML/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

