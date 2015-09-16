---
title: 'go'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, clean-up'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/History
    href: /dom/History
summary: 'Navigates to a relatively positioned history record.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/History/go

---
## Summary

Navigates to a relatively positioned history record.

Method of [dom/History](/dom/History)[dom/History](/dom/History)

## Syntax

``` js
 history.go(relativePosition);
```

## Parameters

### relativePosition

 Data-type
:   Number

 The relative position of a URL in the history list. Out of bounds position (-1 when the current document is the first history record) does nothing.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

An error does not occur if the user tries to go beyond the beginning or end of the history. Instead, the user remains at the current page.

## See also

### Related pages

-   `history`
-   `Reference`
-   `back`
-   `forward`
