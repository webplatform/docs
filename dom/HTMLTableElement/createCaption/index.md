---
title: createCaption
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/createCaption

---
# createCaption

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.createCaption();
```

## Return Value

Returns an object of type DOM Node.

**IHTMLTableCaption**

**caption**

## Examples

This example uses the **createCaption** method to create a **caption**.

    myCaption = document.all.myTable.createCaption()

## Notes

### Remarks

If no caption exists, the **createCaption** method creates an empty table caption, adds it to the table, and returns a pointer to it. If one or more captions already exist, the method returns a pointer to the first one on the list.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

