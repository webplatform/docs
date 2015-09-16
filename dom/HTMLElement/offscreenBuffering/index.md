---
title: 'offscreenBuffering'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, examples, general clean-up of MSDN import'
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
uri: dom/HTMLElement/offscreenBuffering

---
Property of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## Syntax

``` js
var result = element.offscreenBuffering;
element.offscreenBuffering = value;
```

## Notes

### Remarks

The value of the **offscreenBuffering** property determines how the current document is drawn. When the property is set to **true**, objects are added to an offscreen buffer. After all objects are drawn, the contents of the offscreen buffer are made visible to the user. When the property is set to **false**, objects are rendered directly to the screen. By default, Internet Explorer decides when to buffer objects offscreen. In addition, Internet Explorer automatically enables offscreen buffering when Microsoft DirectX-based components are used on the document.

### Syntax

## See also

### Related pages

-   `window`
