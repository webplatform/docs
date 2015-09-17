---
title: 'parseFromString'
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
  - API_Object_Methods
  - DOM
  - Needs_Summary
uri: apis/xhr/methods/parseFromString

---
Method of [apis/xhr/events/load](/apis/xhr/events/load)[apis/xhr/events/load](/apis/xhr/events/load)

## Syntax

``` js
var object = object.parseFromString(xmlSource, mimeType);
```

## Parameters

### xmlSource

 Data-type
:   BSTR

 A string that contains serialized XML source code.

### mimeType

 Data-type
:   BSTR

 A string that identifies one of the following mime types for the source.

## Return Value

Returns an object of type DOM NodeDOM Node

**IHTMLDocument2**

A document object that represents the DOM tree of the XML source.

## Examples

To use the **parseFromString** method, type the following syntax.

``` js
oParser =  new DOMParser();
oDocument = oParser.parseFromString(xmlSource, mimeType);
```

## See also

### Related pages

-   DOMParser[DOMParser](/apis/xhr/objects/DOMParser)
