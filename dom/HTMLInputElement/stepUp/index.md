---
title: stepUp
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLInputElement
    href: /dom/HTMLInputElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLInputElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLInputElement/stepUp

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLInputElement](/dom/HTMLInputElement)[dom/HTMLInputElement](/dom/HTMLInputElement)

## Syntax

``` js
var object = object.stepUp(n);
```

## Parameters

### n

 Data-type
:   any

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

This method can return one of these values.

S\_OK

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Throws an INVALID\_STATE\_ERR exception if the control doesn't support **stepUp**, if the [**Step**](/html/attributes/step) attribute's value is "any", if the current value could not be parsed, or if stepping in the given direction by the given amount would take the value out of range.

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374), Section 4.10.7.4

## See also

### Related pages (MSDN)

-   `HTMLInputElement`
