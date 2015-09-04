---
title: offscreenBuffering
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, examples, general clean-up of MSDN import'
uri: dom/HTMLElement/offscreenBuffering

---
# offscreenBuffering

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLElement](/dom/HTMLElement)</span></span>

## Syntax

``` {.js}
var result = element.offscreenBuffering;
element.offscreenBuffering = value;
```

## Notes

### Remarks

The value of the **offscreenBuffering** property determines how the current document is drawn. When the property is set to **true**, objects are added to an offscreen buffer. After all objects are drawn, the contents of the offscreen buffer are made visible to the user. When the property is set to **false**, objects are rendered directly to the screen. By default, Internet Explorer decides when to buffer objects offscreen. In addition, Internet Explorer automatically enables offscreen buffering when Microsoft DirectX-based components are used on the document.

### Syntax

## See also

### Related pages (MSDN)

-   `window`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

