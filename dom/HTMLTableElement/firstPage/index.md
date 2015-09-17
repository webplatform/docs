---
title: 'firstPage'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'proprietary method; needs clean-up and context'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/HTMLTableElement
    href: /dom/HTMLTableElement
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/HTMLTableElement
standardization_status: Non-Standard
tags:
  - API_Object_Methods
  - DOM
  - Needs_Summary
  - Needs_Examples
uri: dom/HTMLTableElement/firstPage

---
Method of [dom/HTMLTableElement](/dom/HTMLTableElement)[dom/HTMLTableElement](/dom/HTMLTableElement)

## Syntax

``` js
var object = object.firstPage();
```

## Return Value

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

## Notes

### Remarks

The [**dataPageSize**](/html/attributes/dataPageSize) property of the table determines the number of records displayed. You must set the **DATAPAGESIZE** attribute when designing the document, or set the corresponding **dataPageSize** property at run time for this method to have any effect. **Note**  You do not need to check for boundary conditions.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages

-   table[table](/html/elements/table)
