---
title: createTHead
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/createTHead

---
# createTHead

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.createTHead();
```

## Return Value

Returns an object of type DOM Node.

Object

**tHead**

null

## Examples

This example uses the **createTHead** method to create a table header.

    myTHead = document.all.myTable.createTHead()

## Notes

### Remarks

If a **tHead** already exists, **createTHead** returns the existing element. Otherwise, it returns a pointer to the element created.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

