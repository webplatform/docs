---
title: resetStyleInheritance
notes:
  - 'Needs spec reference, example'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return:
    predicate: 'Returns an object of type '
    value: Boolean
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Editor''s Draft'
summary: 'Indicates whether or not the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit. If true, the properties are set to initial value.'
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
uri: dom/shadowdom/ShadowRoot/resetStyleInheritance

---
## <span>Summary</span>

Indicates whether or not the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit. If true, the properties are set to initial value.

Property of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.resetStyleInheritance;
element.resetStyleInheritance = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

If false (default value), the properties continue to inherit. If true, the properties are set to initial value.

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Reflected in the reset-style-inheritance HTML attribute.