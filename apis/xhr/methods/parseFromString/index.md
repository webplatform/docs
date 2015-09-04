---
title: parseFromString
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'Needs summary, spec reference, standardization status'
uri: apis/xhr/methods/parseFromString

---
# parseFromString

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [apis/xhr/events/load](/apis/xhr/events/load)*

## Syntax

``` {.js}
var object = object.parseFromString(xmlSource, mimeType);
```

## Parameters

### xmlSource

 Data-typeÂ
:   BSTR

 A string that contains serialized XML source code.

### mimeType

 Data-typeÂ
:   BSTR

 A string that identifies one of the following mime types for the source.

## Return Value

Returns an object of type DOM Node.

**IHTMLDocument2**

A document object that represents the DOM tree of the XML source.

## Examples

To use the **parseFromString** method, type the following syntax.

``` {.js}
oParser =  new DOMParser();
oDocument = oParser.parseFromString(xmlSource, mimeType);
```

## See also

### Related pages (MSDN)

-   `DOMParser`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

