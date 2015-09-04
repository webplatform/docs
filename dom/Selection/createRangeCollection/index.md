---
title: createRangeCollection
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Out of Date'
notes:
  - "there is no createRangeCollection Method of the HTMLSelection object.\nPlease delete."
uri: dom/Selection/createRangeCollection

---
# createRangeCollection

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Selection](/dom/Selection)*

## Syntax

``` {.js}
var object = object.createRangeCollection();
```

## Return Value

Returns an object of type DOM Node.

Object

Returns a collection of [**TextRange**](/dom/TextRange) objects.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Host applications can provide a multiple selection mechanism and can return a collection of [**TextRange**](/dom/TextRange) objects that represents discontinuous selections. The host application provides the collection through the **ISegmentList** interface. *MSHTML* requests this interface through the **ISelectionServices** interface. Microsoft Internet Explorer 5.5 does not provide multiple selection. The default implementation of this method returns a collection consisting of a single [**TextRange**](/dom/TextRange) object.

### Syntax

### Standards information

There are no standards that apply here.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

