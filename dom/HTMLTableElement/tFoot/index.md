---
title: 'tFoot'
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
  - API_Object_Properties
  - DOM
uri: dom/HTMLTableElement/tFoot

---
Property of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var result = element.tFoot;
element.tFoot = value;
```

## Examples

This example sets the color of the **tFoot** object to blue.

``` html
document.all.myTable.tFoot.style.color = "blue"
```

## Notes

### Remarks

If the table doesn't have a foot section, the value for the property is null. If multiple table feet are listed in on a document, only the first one is treated as the foot of the table.

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## See also

### Related pages

-   table[table](/html/elements/table)
