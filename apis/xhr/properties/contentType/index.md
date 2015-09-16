---
title: 'contentType'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, usage, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/xhr/properties
    href: /apis/xhr/properties
tags:
  - API
  - Object
  - Properties
  - DOM
uri: apis/xhr/properties/contentType

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Property of [apis/xhr/properties](/apis/xhr/properties)[apis/xhr/properties](/apis/xhr/properties)

## Syntax

``` js
var result = element.contentType;
element.contentType = value;
```

## Examples

``` js
// 1. Create XDR object
xdr = new XDomainRequest();

// 2. Open connection with server using GET method
xdr.open("GET", "http://www.contoso.com/xdr.txt");

// 3. Display the content-type
alert(xdr.contentType);
```

## See also

### Related pages

-   `Reference`
-   `IHTMLXDomainRequest`
-   `XDomainRequest`
-   `Conceptual`
-   `Introducing Cross-domain Request`
