---
title: onmessage
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/workers/Worker
    href: /apis/workers/Worker
  return:
    predicate: 'Returns an object of type '
    value: ''
    href: /apis/workers/Worker
standardization_status: 'W3C Editor''s Draft'
summary: 'An event listener to be called when a message is received from the worker.'
tags:
  0: API
  1: Object
  2: Properties
  4: Webworkers
uri: apis/workers/Worker/onmessage

---
## Summary

An event listener to be called when a message is received from the worker.

Property of [apis/workers/Worker](/apis/workers/Worker)[apis/workers/Worker](/apis/workers/Worker)

## Syntax

**Note**: This property is read-only.

``` js
var result = object.onmessage;
```

## Return Value

Returns an object of type

EventHandler

**Needs Examples**: This section should include examples.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
