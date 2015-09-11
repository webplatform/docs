---
title: forward
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Summary, examples, compatibility, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/History
    href: /dom/History
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/History
standardization_status: Non-Standard
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/History/forward

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/History](/dom/History)[dom/History](/dom/History)

## <span>Syntax</span>

``` js
var object = object.forward();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

Type: **HRESULT**

If this method succeeds, it returns **S\_OK**. Otherwise, it returns an **HRESULT** error code.

**Needs Examples**: This section should include examples.

## <span>Notes</span>

### <span>Remarks</span>

This method performs the same action as when a user clicks the **Forward** button in the browser. Calling the **forward** method works the same as calling the **go** method with a parameter of `1`. An error does not occur if the user tries to go beyond the end of the history. Instead, the user remains at the current page.

### <span>Syntax</span>

### <span>Standards information</span>

There are no standards that apply here.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `history`
-   `Reference`
-   `back`
-   `go`
