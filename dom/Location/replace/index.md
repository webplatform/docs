---
title: 'replace'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'examples, compatibility, standards'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Location
    href: /dom/Location
summary: 'Replaces the current document by loading another document at the specified URL.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Location/replace

---
## Summary

Replaces the current document by loading another document at the specified URL.

Method of [dom/Location](/dom/Location)[dom/Location](/dom/Location)

## Syntax

``` js
 location.replace(/* see parameter list */);
```

## Parameters

### url

 Data-type
:   String

 The URL to insert into the session history.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

When a document is replaced, it is also removed from the **history** object. Moreover, the user interface navigation methods, such as the Back and Forward buttons, will no longer access the URL.
