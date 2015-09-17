---
title: 'onprogress'
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
uri: dom/Element/onprogress

---
Property of [dom/Element](/dom/Element)[dom/Element](/dom/Element)

## Syntax

``` js
var result = element.onprogress;
element.onprogress = value;
```

## Notes

### Remarks

This event reports back the number of bytes loaded from the stream so far. You can use this information to update a progress bar in your application.

### Syntax

### Event handler parameters

*pEvtObj* [in]
:   Type: ****IHTMLEventObj****

## See also

### Related pages

-   FileReader[FileReader](/apis/file/FileReader)
