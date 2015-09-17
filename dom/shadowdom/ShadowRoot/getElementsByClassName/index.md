---
title: 'getElementsByClassName'
notes:
  - 'Needs spec reference, example'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return_type:
    predicate: 'Returns an object of type  '
    value: Object
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Editor''s Draft'
summary: 'Just like Document/getElementsByClassName except that it only works within the scope of this ShadowRoot''s shadow tree.'
tags:
  - API_Object_Methods
  - DOM
  - Shadow_DOM
  - Needs_Examples
uri: dom/shadowdom/ShadowRoot/getElementsByClassName

---
## Summary

Just like Document/getElementsByClassName except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## Syntax

``` js
var result = element.getElementsByClassName(classNames);
```

## Parameters

### classNames

 Data-type
:   String

 A space separated list of classes.

## Return Value

Returns an object of type ObjectObject

A live [HTMLCollection](/dom/HTMLCollection) of elements with the given class names.

## Notes

Use of this method is discouraged. See [HTMLCollection](/dom/HTMLCollection). However, that article has not been vetted for vendor bias, it is an unreviewed import, and the performance implications described may be browser (IE) specific.
