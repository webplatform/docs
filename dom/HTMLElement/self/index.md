---
title: 'self'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'needs summary, general clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLElement/self

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.self;
element.self = value;
```

## Notes

### Remarks

You can use the property to explicitly refer to the current window or frame. To improve scripting efficiency, you also can use it to make implicit window references explicit.

### Syntax

## See also

### Related pages

-   `frame`
-   `window`
