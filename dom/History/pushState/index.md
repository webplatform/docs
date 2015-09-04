---
title: pushState
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Not Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Examples, compatibility, clean-up of MSDN import'
summary: 'Programmatically push a document state (including URI and document title) onto the user agent''s history.'
uri: dom/History/pushState

---
# pushState

## Summary

Programmatically push a document state (including URI and document title) onto the user agent's history.

*Method of [dom/History](/dom/History)*

## Syntax

``` {.js}
 history.pushState(statedata, title, url);
```

## Parameters

### statedata

 Data-typeÂ
:   any

 The data to push onto the session history.

### title

 Data-typeÂ
:   any

 The desired title for the data.

### url

 Data-typeÂ
:   any

*(Optional)*

An optional URL to associate with the data.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[HTML 5](http://www.w3.org/TR/html5/browsers.html#dom-history-pushstate)
:   W3C Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

