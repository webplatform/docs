---
title: lastPage
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'proprietary method; needs clean-up and context'
uri: dom/HTMLTableElement/lastPage

---
# lastPage

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/HTMLTableElement](/dom/HTMLTableElement)*

## Syntax

``` {.js}
var object = object.lastPage();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

The [**dataPageSize**](/html/attributes/dataPageSize) property of the table determines the number of records displayed. You must set the **DATAPAGESIZE** attribute when designing the document, or set the corresponding **dataPageSize** property at run time for this method to have any effect. **Note**  You do not need to check for boundary conditions.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `table`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

