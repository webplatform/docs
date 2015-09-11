---
title: getElementsByClassName
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
  - API
  - Object
  - Methods
  - DOM
  - Shadow
uri: dom/shadowdom/ShadowRoot/getElementsByClassName

---
## <span>Summary</span>

Just like Document/getElementsByClassName except that it only works within the scope of this ShadowRoot's shadow tree.

Method of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.getElementsByClassName(classNames);
```

## <span>Parameters</span>

### <span>classNames</span>

 Data-type
:   String

 A space separated list of classes.

## <span>Return Value</span>

Returns an object of type ObjectObject

A live [HTMLCollection](/dom/HTMLCollection) of elements with the given class names.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

Use of this method is discouraged. See [HTMLCollection](/dom/HTMLCollection). However, that article has not been vetted for vendor bias, it is an unreviewed import, and the performance implications described may be browser (IE) specific.