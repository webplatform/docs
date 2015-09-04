---
title: draggable
tags:
  - API
  - Object
  - Properties
readiness: 'Almost Ready'
standardization_status: 'W3C Working Draft'
notes:
  - 'examples, compatibility'
summary: 'Gets or sets whether an element can be dragged and dropped.'
uri: dom/HTMLElement/draggable

---
# draggable

## Summary

Gets or sets whether an element can be dragged and dropped.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var draggable = element.draggable;
element.draggable = draggable;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

Whether the element is draggable.

**Needs Examples**: This section should include examples.

## Usage

     Use this property to allow or disallow an element to be dragged and dropped.

## Notes

The default value for most elements is **false**. [a](/html/elements/a) and [img](/html/elements/img) elements are draggable by default.

## Related specifications

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
[HTML5](http://www.w3.org/TR/html5)
:   Working Draft

