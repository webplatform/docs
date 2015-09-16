---
title: draggable
notes:
  - 'examples, compatibility'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/HTMLElement
standardization_status: 'W3C Working Draft'
summary: 'Gets or sets whether an element can be dragged and dropped.'
tags:
  - API
  - Object
  - Properties
uri: dom/HTMLElement/draggable

---
## Summary

Gets or sets whether an element can be dragged and dropped.

Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var draggable = element.draggable;
element.draggable = draggable;
```

## Return Value

Returns an object of type BooleanBoolean

Whether the element is draggable.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to allow or disallow an element to be dragged and dropped.

## Notes

The default value for most elements is **false**. [a](/html/elements/a) and [img](/html/elements/img) elements are draggable by default.

## Related specifications

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5)
:   Working Draft

