---
title: go
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
## <span>Summary</span>

Navigates to a relatively positioned history record.

Method of [dom/History](/dom/History)[dom/History](/dom/History)

## <span>Syntax</span>

``` js
 history.go(relativePosition);
```

## <span>Parameters</span>

### <span>relativePosition</span>

 Data-type
:   Number

 The relative position of a URL in the history list. Out of bounds position (-1 when the current document is the first history record) does nothing.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

An error does not occur if the user tries to go beyond the beginning or end of the history. Instead, the user remains at the current page.

## <span>See also</span>

### <span>Related pages (MSDN)</span>

-   `history`
-   `Reference`
-   `back`
-   `forward`
