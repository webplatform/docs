---
title: namedItem
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN content'
uri: dom/HTMLElement/namedItem

---
# namedItem

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLElement](/dom/HTMLElement)*

## Syntax

``` {.js}
var object = object.namedItem(name);
```

## Parameters

### name

 Data-type�
:   BSTR

 A **String** that specifies the [**name**](/html/attributes/name) or [**id**](/html/attributes/id) property of the object to retrieve. A collection is returned if more than one match is made.

## Return Value

Returns an object of type DOM Node.

Object

## Examples

The following example shows how to use the **namedItem** method to retrieve a **div** and change its [**innerText**](/dom/HTMLElement/innerText) property.

    <div id="oDIV1">This text will not change.</div>
    <div id="oDIV2">This text will change.</div>
    <button onclick="document.all.namedItem('oDIV2').innerHTML='Changed!';">
       Change Option
    </button>

## Notes

### Remarks

Windows Internet Explorer 8 and later. In IE8 Standards mode, the **namedItem** method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched Defining Document Compatibility. The **namedItem** method was introduced in Microsoft Internet Explorer 6. The **namedItem** method does not return collections if more than one named item is found; instead, it returns the first case-insensitive matched **element**. This method first searches for an object with a matching [**id**](/html/attributes/id) attribute. If a match is not found, the method searches for an object with a matching [**name**](/html/attributes/name) attribute, but only on those elements that are allowed a name attribute.

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

