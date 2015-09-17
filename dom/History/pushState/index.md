---
title: 'pushState'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Examples, compatibility, clean-up of MSDN import'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/History
    href: /dom/History
standardization_status: 'W3C Recommendation'
summary: 'Programmatically push a document state (including URI and document title) onto the user agent''s history.'
tags:
  - API_Object_Methods
  - DOM
  - Needs_Examples
uri: dom/History/pushState

---
## Summary

Programmatically push a document state (including URI and document title) onto the user agent's history.

Method of [dom/History](/dom/History)[dom/History](/dom/History)

## Syntax

``` js
 history.pushState(statedata, title, url);
```

## Parameters

### statedata

 Data-type
:   any

 The data to push onto the session history.

### title

 Data-type
:   any

 The desired title for the data.

### url

 Data-type
:   any

(Optional)

An optional URL to associate with the data.

## Return Value

No return value

## Related specifications

[HTML 5](http://www.w3.org/TR/html5/browsers.html#dom-history-pushstate)
:   W3C Recommendation
