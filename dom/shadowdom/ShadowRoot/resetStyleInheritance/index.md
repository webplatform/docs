---
title: resetStyleInheritance
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
readiness: 'In Progress'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs spec reference, example'
summary: 'Indicates whether or not the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit. If true, the properties are set to initial value.'
uri: dom/shadowdom/ShadowRoot/resetStyleInheritance

---
# resetStyleInheritance

## Summary

Indicates whether or not the inheritable CSS properties are set to the initial value at the shadow boundary. If false (default value), the properties continue to inherit. If true, the properties are set to initial value.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)</span></span>

## Syntax

``` {.js}
var result = element.resetStyleInheritance;
element.resetStyleInheritance = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

If false (default value), the properties continue to inherit. If true, the properties are set to initial value.

**Needs Examples**: This section should include examples.

## Usage

     Reflected in the reset-style-inheritance HTML attribute.

