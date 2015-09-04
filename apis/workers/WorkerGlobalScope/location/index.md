---
title: location
tags:
  0: API
  1: Object
  2: Properties
  4: Webworkers
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs example'
summary: 'Returns the WorkerLocation object created for the WorkerGlobalScope object when the worker was created.'
uri: apis/workers/WorkerGlobalScope/location

---
# location

## Summary

Returns the WorkerLocation object created for the WorkerGlobalScope object when the worker was created.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var result = object.location;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">String</span></span>

Represents the absolute URL of the script that was used to initialize the worker, after any redirects.

**Needs Examples**: This section should include examples.

## Related specifications

Specification
:   Status
[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

