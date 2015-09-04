---
title: item
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'Needs summary, examples, syntax, compat, spec'
uri: dom/Element/item

---
# item

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var object = object.item(/* see parameter list */);
```

## Parameters

### index

 Data-type�
:   any

 An **Integer** that specifies the zero-based index of the object to get.

## Return Value

Returns an object of type DOM Node.

**IHTMLElement**

**Needs Examples**: This section should include examples.

## Notes

### Remarks

**Note**   if given a string that is not a numeric index, this method will return the object at index `0`. This method returns S\_OK, even if the element is not found. Check the value of the IDispatch pointer returned by this call. If the value of the pointer is NULL; the element was not found, and the call was not successful.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

