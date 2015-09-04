---
title: tHead
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/tHead

---
# tHead

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLTableElement](/dom/HTMLTableElement)</span></span>

## Syntax

``` {.js}
var result = element.tHead;
element.tHead = value;
```

## Examples

This example sets the color of the **tHead** object to blue.

    document.all.myTable.tHead.style.color = "blue"

## Notes

### Remarks

If the table doesn't have a head section, the value for the property is null. If multiple table heads are listed in on a document, only the first one is treated as the head of the table.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

