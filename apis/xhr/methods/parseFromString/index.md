---
title: parseFromString
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, spec reference, standardization status'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/xhr/events/load
    href: /apis/xhr/events/load
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /apis/xhr/events/load
tags:
  - API
  - Object
  - Methods
  - DOM
uri: apis/xhr/methods/parseFromString

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [apis/xhr/events/load](/apis/xhr/events/load)[apis/xhr/events/load](/apis/xhr/events/load)

## <span>Syntax</span>

``` js
var object = object.parseFromString(xmlSource, mimeType);
```

## <span>Parameters</span>

### <span>xmlSource</span>

 Data-type
:   BSTR

 A string that contains serialized XML source code.

### <span>mimeType</span>

 Data-type
:   BSTR

 A string that identifies one of the following mime types for the source.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

**IHTMLDocument2**

A document object that represents the DOM tree of the XML source.

## <span>Examples</span>

To use the **parseFromString** method, type the following syntax.

``` js
oParser =  new DOMParser();
oDocument = oParser.parseFromString(xmlSource, mimeType);
```

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `DOMParser`
