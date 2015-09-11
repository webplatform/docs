---
title: blur
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLElement
    href: /dom/HTMLElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLElement
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/HTMLElement/blur

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var object = object.blur();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

This method shifts focus away from the element it is applied to but does not set focus on the next element in the tab order. In Microsoft Internet Explorer 5 and greater, elements that expose the **blur** method must have the [**TABINDEX**](/html/attributes/tabIndex) attribute set.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5
