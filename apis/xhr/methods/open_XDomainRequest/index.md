---
title: open (XDomainRequest)
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status. Probably should be renamed to remove (XDomainRequest) from the URL.'
uri: 'apis/xhr/methods/open (XDomainRequest)'

---
# open (XDomainRequest)

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)*

## Syntax

``` {.js}
var object = object.open (XDomainRequest)(bstrMethod, bstrUrl);
```

## Parameters

### bstrMethod

 Data-typeÂ
:   BSTR

 GET method.

POST method.

### bstrUrl

 Data-typeÂ
:   BSTR

 The server URL.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

``` {.js}
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

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

