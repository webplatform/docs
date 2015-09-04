---
title: contentType
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, usage, spec reference, standardization status'
uri: apis/xhr/properties/contentType

---
# contentType

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/xhr/properties](/apis/xhr/properties)</span></span>

## Syntax

``` {.js}
var result = element.contentType;
element.contentType = value;
```

## Examples

``` {.js}
// 1. Create XDR object
xdr = new XDomainRequest();

// 2. Open connection with server using GET method
xdr.open("GET", "http://www.contoso.com/xdr.txt");

// 3. Display the content-type
alert(xdr.contentType);
```

## See also

### Related pages (MSDN)

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`
-   `Conceptual`
-   `Introducing Cross-domain Request`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

