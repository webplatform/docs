---
title: tBodies
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Not Ready'
standardization_status: Unknown
notes:
  - 'summary, clean-up of MSDN import'
uri: dom/HTMLTableElement/tBodies

---
# tBodies

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/HTMLTableElement](/dom/HTMLTableElement)</span></span>

## Syntax

``` {.js}
var result = element.tBodies;
element.tBodies = value;
```

## Examples

This example shows how to put text in the first cell in the first row of the first **tBody** object in the [**table**](/html/elements/table). For each **table**, an initial **tBody** object is synthesized in the HTML tree even if a **tBody** element does not exist in the HTML source.

    document.all.oTable.tBodies[0].rows[0].cells[0].innerText =
       "Text for the first table cell";

## Notes

### Remarks

This collection can be indexed by name ([**ID**](/html/attributes/id)). If duplicate names are found, a collection of those named items is returned. Collections of duplicate names must be referenced subsequently by ordinal position.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

