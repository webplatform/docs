---
title: send (XDomainRequest)
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs spec reference, standardization status. Probably should be renamed to remove (XDomainRequest) from the URL.'
uri: 'apis/xhr/methods/send (XDomainRequest)'

---
# send (XDomainRequest)

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [apis/xhr/objects/XDomainRequest](/apis/xhr/objects/XDomainRequest)*

## Syntax

``` {.js}
var object = object.send (XDomainRequest)(varBody);
```

## Parameters

### varBody

 Data-typeÂ
:   VARIANT

 Receives a **Variant** of type **String** containing the data to transmit to the server. If omitted, the behavior is identical to that of sending an empty string ( "" ).

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

## See also

### Related pages (MSDN)

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

