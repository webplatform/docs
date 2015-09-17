---
title: 'onloadstart'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, examples, spec, and compat'
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
uri: dom/Element/onloadstart

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.onloadstart;
element.onloadstart = value;
```

## Notes

### Remarks

This event fires when a method starts to read a [**Blob**](/apis/file/Blob) object. This event is dispatched first and occurs only one time. Indicates that the creation or load of an object is started.

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   FileReader[FileReader](/apis/file/FileReader)
