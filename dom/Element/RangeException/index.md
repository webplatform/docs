---
title: RangeException
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Summary, examples, compat, better spec link'
uri: dom/Element/RangeException

---
# RangeException

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/Element](/dom/Element)*

## Syntax

``` {.js}
var object = object.RangeException(fragment, retVal);
```

## Parameters

### fragment

 Data-typeÂ
:   any

 String containing HTML to be parsed.

### retVal

 Data-typeÂ
:   any

 A document fragment representing the parsed HTML.

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

This method can return one of these values.

Return code
:   Description
S\_OK
:   The operation completed successfully.
W3CException\_INVALID\_STATE\_ERR
:   Throws this exception if the range has been detached.

Â

DocumentFragment

A document fragment representing the parsed HTML.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

When inserting elements into a DOM structure, some elements behave according to their context. Using createContextualFragment, you can ensure the parsed HTML will work as expected when inserted or added to the document.

### Syntax

### Standards information

-   [HTML5 A vocabulary and associated APIs for HTML and XHTML](http://go.microsoft.com/fwlink/p/?linkid=221374)

## See also

### Related pages (MSDN)

-   `Range`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

