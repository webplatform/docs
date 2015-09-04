---
title: getElementsByClassName
tags:
  - API
  - Object
  - Methods
  - DOM
  - Shadow
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs spec reference, example'
summary: 'Just like Document/getElementsByClassName except that it only works within the scope of this ShadowRoot''s shadow tree.'
uri: dom/shadowdom/ShadowRoot/getElementsByClassName

---
# getElementsByClassName

## Summary

Just like Document/getElementsByClassName except that it only works within the scope of this ShadowRoot's shadow tree.

*Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)*

## Syntax

``` {.js}
var result = element.getElementsByClassName(classNames);
```

## Parameters

### classNames

 Data-typeÂ
:   String

 A space separated list of classes.

## Return Value

Returns an object of type Object.

A live [HTMLCollection](/dom/HTMLCollection) of elements with the given class names.

**Needs Examples**: This section should include examples.

## Notes

Use of this method is discouraged. See [HTMLCollection](/dom/HTMLCollection). However, that article has not been vetted for vendor bias, it is an unreviewed import, and the performance implications described may be browser (IE) specific.

