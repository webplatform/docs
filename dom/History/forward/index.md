---
title: forward
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
standardization_status: Non-Standard
notes:
  - 'Summary, examples, compatibility, clean-up of MSDN import'
uri: dom/History/forward

---
# forward

**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

*Method of [dom/History](/dom/History)*

## Syntax

``` {.js}
var object = object.forward();
```

## Return Value

Returns an object of type DOM Node.

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## Notes

### Remarks

This method performs the same action as when a user clicks the **Forward** button in the browser. Calling the **forward** method works the same as calling the **go** method with a parameter of `1`. An error does not occur if the user tries to go beyond the end of the history. Instead, the user remains at the current page.

### Syntax

### Standards information

There are no standards that apply here.

## See also

### Related pages (MSDN)

-   `history`
-   `Reference`
-   `back`
-   `go`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

