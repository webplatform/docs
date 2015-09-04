---
title: deleteTFoot
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/deleteTFoot

---
# deleteTFoot

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.deleteTFoot();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Examples

This example uses the **deleteTFoot** method to delete the **tFoot** element from the table.

    document.all.myTable.deleteTFoot()

## Notes

### Remarks

If only one **tFoot** element exists in the source, the **deleteTFoot** method deletes the table footer. If multiple **tFoot** elements have been defined, the next **tFoot** element in the source order is promoted as the table footer.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

