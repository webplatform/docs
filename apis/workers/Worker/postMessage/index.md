---
title: 'postMessage'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/workers/Worker
    href: /apis/workers/Worker
standardization_status: 'W3C Editor''s Draft'
summary: 'Posts a message to the worker with which the object is associated.'
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
uri: apis/workers/Worker/postMessage

---
## Summary

Posts a message to the worker with which the object is associated.

Method of [apis/workers/Worker](/apis/workers/Worker)[apis/workers/Worker](/apis/workers/Worker)

## Syntax

``` js
 object.postMessage(message, transfer);
```

## Parameters

### message

 Data-type
:   any

 This argument can be structured data, e.g.: `worker.postMessage({opcode: 'activate', device: 1938, parameters: [23, 102]});`

### transfer

 Data-type
:   any

(Optional)

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

A message can be a JavaScript primitive, object, or array, but not a function.

## Related specifications

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
