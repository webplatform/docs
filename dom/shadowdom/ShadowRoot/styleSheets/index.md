---
title: styleSheets
notes:
  - 'Needs spec reference, usage, example'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/shadowdom/ShadowRoot
    href: /dom/shadowdom/ShadowRoot
  return:
    predicate: 'Returns an object of type '
    value: StyleSheetList
    href: /dom/shadowdom/ShadowRoot
standardization_status: 'W3C Editor''s Draft'
summary: 'Represents the shadow root style sheets.'
tags:
  0: API
  1: Object
  2: Properties
  4: DOM
  5: Shadow
uri: dom/shadowdom/ShadowRoot/styleSheets

---
## <span>Summary</span>

Represents the shadow root style sheets.

Property of [dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)[dom/shadowdom/ShadowRoot](/dom/shadowdom/ShadowRoot)

## <span>Syntax</span>

``` js
var result = element.styleSheets;
element.styleSheets = value;
```

## <span>Return Value</span>

Returns an object of type StyleSheetListStyleSheetList

On getting, the attribute must return a StyleSheetList sequence containing the shadow root style sheets.

**Needs Examples**: This section should include examples.

