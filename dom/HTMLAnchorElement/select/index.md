---
title: 'select'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLAnchorElement
    href: /dom/HTMLAnchorElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLAnchorElement
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/HTMLAnchorElement/select

---
Method of [dom/HTMLAnchorElement](/dom/HTMLAnchorElement)[dom/HTMLAnchorElement](/dom/HTMLAnchorElement)

## Syntax

``` js
var object = object.select();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Notes

### Remarks

Use this method with the [**focus**](/dom/HTMLElement/focus) method to highlight a field and position the cursor for a user response.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
