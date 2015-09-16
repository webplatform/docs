---
title: open (XDomainRequest)
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status. Probably should be renamed to remove (XDomainRequest) from the URL.'
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
uri: 'apis/xhr/methods/open (XDomainRequest)'

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)[apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)

## Syntax

``` js
var object = object.open (XDomainRequest)(bstrMethod, bstrUrl);
```

## Parameters

### bstrMethod

 Data-type
:   BSTR

 GET method.

POST method.

### bstrUrl

 Data-type
:   BSTR

 The server URL.

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

## Notes

### Remarks

Requires an XDomainRequest object.

## See also

### Related pages (MSDN)

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`
-   `Other Resources`
-   `W3C Architecture: Naming and Addressing: URIs, URLs, ...`
-   `RFC2616: Hypertext Transfer Protocol -- HTTP/1.1`
