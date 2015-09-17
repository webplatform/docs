---
title: 'submit'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLFormElement
    href: /dom/HTMLFormElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLFormElement
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/HTMLFormElement/submit

---
Method of [dom/HTMLFormElement](/dom/HTMLFormElement)[dom/HTMLFormElement](/dom/HTMLFormElement)

## Syntax

``` js
var object = object.submit();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Notes

### Remarks

The **submit** method does not invoke the **onsubmit** event handler. Call the **onsubmit** event handler directly.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages

-   `form`
-   `Reference`
-   `input`
-   reset[reset](/dom/HTMLFormElement/reset)
