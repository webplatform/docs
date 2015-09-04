---
title: go
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
notes:
  - 'examples, clean-up'
summary: 'Navigates to a relatively positioned history record.'
uri: dom/History/go

---
# go

## Summary

Navigates to a relatively positioned history record.

*Method of [dom/History](/dom/History)*

## Syntax

``` {.js}
 history.go(relativePosition);
```

## Parameters

### relativePosition

 Data-typeÂ
:   Number

 The relative position of a URL in the history list. Out of bounds position (-1 when the current document is the first history record) does nothing.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

An error does not occur if the user tries to go beyond the beginning or end of the history. Instead, the user remains at the current page.

## See also

### Related pages (MSDN)

-   `history`
-   `Reference`
-   `back`
-   `forward`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

