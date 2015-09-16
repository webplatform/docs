---
title: location
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
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/workers/WorkerGlobalScope
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the WorkerLocation object created for the WorkerGlobalScope object when the worker was created.'
tags:
  0: API
  1: Object
  2: Properties
  4: Webworkers
uri: apis/workers/WorkerGlobalScope/location

---
## Summary

Returns the WorkerLocation object created for the WorkerGlobalScope object when the worker was created.

Property of [apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)[apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.location;
```

## Return Value

Returns an object of type StringString

Represents the absolute URL of the script that was used to initialize the worker, after any redirects.

**Needs Examples**: This section should include examples.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
