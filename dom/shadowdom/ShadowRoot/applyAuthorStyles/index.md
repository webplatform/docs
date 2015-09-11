---
title: applyAuthorStyles
notes:
  - 'Needs spec reference, standardization status, example'
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
summary: 'Indicates whether the rules in author styles associated with the element''s document apply to the shadow tree. If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.'
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
uri: dom/shadowdom/ShadowRoot/applyAuthorStyles

---
## <span>Summary</span>

Indicates whether the rules in author styles associated with the element's document apply to the shadow tree. If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.

Property of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.applyAuthorStyles;
element.applyAuthorStyles = value;
```

## <span>Return Value</span>

Returns an object of type BooleanBoolean

If false (default value), the author styles are not applied to the shadow tree. If true, the author styles are applied.

**Needs Examples**: This section should include examples.

