---
title: 'typeDetail'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Not in the spec or MSDN/MDN documentation\nPlease delete"
readiness: 'Out of Date'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Selection
    href: /dom/Selection
tags:
  - API_Object_Properties
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/Selection/typeDetail

---
Property of [dom/Selection](/dom/Selection)[dom/Selection](/dom/Selection)

## Syntax

``` js
var result = element.typeDetail;
element.typeDetail = value;
```

## Notes

### Remarks

The default implementation of this property returns a value of `undefined`. Host applications can provide a custom selection mechanism and can provide a value for this property that indicates the selection type. *MSHTML* requests the selection type from the host application by calling **GetTypeDetail**.

### Syntax
