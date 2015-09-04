---
title: applyAuthorStyles
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
readiness: 'In Progress'
notes:
  - 'Needs spec reference, standardization status, example'
summary: 'Indicates whether the rules in author styles associated with the element''s document apply to the shadow tree. If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.'
uri: dom/shadowdom/ShadowRoot/applyAuthorStyles

---
# applyAuthorStyles

## Summary

Indicates whether the rules in author styles associated with the element's document apply to the shadow tree. If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)</span></span>

## Syntax

``` {.js}
var result = element.applyAuthorStyles;
element.applyAuthorStyles = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">Boolean</span></span>

If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.

**Needs Examples**: This section should include examples.

