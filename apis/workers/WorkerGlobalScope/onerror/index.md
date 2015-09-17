---
title: 'onerror'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/workers/WorkerGlobalScope
    href: /apis/workers/WorkerGlobalScope
standardization_status: 'W3C Editor''s Draft'
summary: 'An event listener to be called when an error occurs.'
tags:
  - API_Object_Properties
  - API
  - Webworkers
  - Needs_Examples
uri: apis/workers/WorkerGlobalScope/onerror

---
## Summary

An event listener to be called when an error occurs.

Property of [apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)[apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.onerror;
```

## Notes

Returns an **error** object with property values of **filename**, **lineno**, and **message**.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
