---
title: 'onload'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec and compat'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Element
    href: /dom/Element
tags:
  - API_Object_Properties
  - Needs_Summary
  - Needs_Examples
uri: dom/Element/onload

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.onload;
element.onload = value;
```

## Notes

### Remarks

This event fires when a method finishes the read of a [**Blob**](/apis/file/Blob) object. If the operation fails, **onload** does not fire, but instead, the **onloadend** and **onerror** events fire.

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   FileReader[FileReader](/apis/file/FileReader)
