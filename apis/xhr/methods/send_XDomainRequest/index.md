---
title: send (XDomainRequest)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs spec reference, standardization status. Probably should be renamed to remove (XDomainRequest) from the URL.'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/objects/XDomainRequest
    href: /apis/xhr/objects/XDomainRequest
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/xhr/objects/XDomainRequest
tags:
  - API
  - Object
  - Methods
  - DOM
uri: 'apis/xhr/methods/send (XDomainRequest)'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)[apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)

## Syntax

``` js
var object = object.send (XDomainRequest)(varBody);
```

## Parameters

### varBody

 Data-type
:   VARIANT

 Receives a **Variant** of type **String** containing the data to transmit to the server. If omitted, the behavior is identical to that of sending an empty string ( "" ).

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` js
// 1. Create XDR object
xdr = new XDomainRequest();

// 2. Open connection with server using POST method
xdr.open("POST", "http://www.contoso.com/xdr.txt");

// 3. Send string data to server
xdr.send("data to be processed");
```

## See also

### Related pages (MSDN)

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`
