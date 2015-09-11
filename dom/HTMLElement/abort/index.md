---
title: abort
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
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
uri: dom/HTMLElement/abort

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/HTMLElement](/dom/HTMLElement)[dom/HTMLElement](/dom/HTMLElement)

## <span>Syntax</span>

``` js
var object = object.abort();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## <span>Examples</span>

A simple abort example.

``` js
// 1. Create XDR object
xdr = new XDomainRequest();
// 2. Open connection with server using POST method
xdr.open("POST", "http://www.contoso.com/xdr.txt");
// 3. Send string data to server
xdr.send("data to be processed");
// 4. abort
xdr.abort();
```

## <span>Notes</span>

### <span>Remarks</span>

The abort method may be called in the time after the send method has been called, and before the onload event is raised. An error is returned if it is called outside of this interval.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`
