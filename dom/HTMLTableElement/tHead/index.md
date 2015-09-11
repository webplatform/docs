---
title: tHead
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
uri: dom/HTMLTableElement/tHead

---
Property of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## <span>Syntax</span>

``` js
var result = element.tHead;
element.tHead = value;
```

## <span>Examples</span>

This example sets the color of the **tHead** object to blue.

``` html
document.all.myTable.tHead.style.color = "blue"
```

## <span>Notes</span>

### <span>Remarks</span>

If the table doesn't have a head section, the value for the property is null. If multiple table heads are listed in on a document, only the first one is treated as the head of the table.

### <span>Syntax</span>

### <span>Standards information</span>

-   [Document Object Model (DOM) Level 1 Specification](http://go.microsoft.com/fwlink/p/?linkid=161725), Section 2.5.5

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `table`
