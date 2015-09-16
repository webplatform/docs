---
title: tBodies
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'summary, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
standardization_status: Unknown
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/HTMLTableElement/tBodies

---
Property of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var result = element.tBodies;
element.tBodies = value;
```

## Examples

This example shows how to put text in the first cell in the first row of the first **tBody** object in the [**table**](/html/elements/table). For each **table**, an initial **tBody** object is synthesized in the HTML tree even if a **tBody** element does not exist in the HTML source.

``` html
document.all.oTable.tBodies[0].rows[0].cells[0].innerText =
   "Text for the first table cell";
```

## Notes

### Remarks

This collection can be indexed by name ([**ID**](/html/attributes/id)). If duplicate names are found, a collection of those named items is returned. Collections of duplicate names must be referenced subsequently by ordinal position.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.6.5

## See also

### Related pages

-   `table`
