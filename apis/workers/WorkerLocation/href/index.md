---
title: href
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/workers/WorkerLocation
    href: /apis/workers/WorkerLocation
  return:
    predicate: 'Returns an object of type '
    value: String
    href: /apis/workers/WorkerLocation
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the absolute URL that the object represents.'
tags:
  0: API
  1: Object
  2: Properties
  4: Webworkers
uri: apis/workers/WorkerLocation/href

---
## Summary

Returns the absolute URL that the object represents.

Property of [apis/workers/WorkerLocation](/apis/workers/WorkerLocation)[apis/workers/WorkerLocation](/apis/workers/WorkerLocation)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.href;
```

## Return Value

Returns an object of type StringString

**Needs Examples**: This section should include examples.

## Notes

The **href** is the entire string of the URL.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
