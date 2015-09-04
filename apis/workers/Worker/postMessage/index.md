---
title: postMessage
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs example'
summary: 'Posts a message to the worker with which the object is associated.'
uri: apis/workers/Worker/postMessage

---
# postMessage

## Summary

Posts a message to the worker with which the object is associated.

*Method of [apis/workers/Worker](/apis/workers/Worker)*

## Syntax

``` {.js}
 object.postMessage(message, transfer);
```

## Parameters

### message

 Data-typeÂ
:   any

 This argument can be structured data, e.g.: `worker.postMessage({opcode: 'activate', device: 1938, parameters: [23, 102]});`

### transfer

 Data-typeÂ
:   any

*(Optional)*

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

A message can be a JavaScript primitive, object, or array, but not a function.

## Related specifications

Specification
:   Status
[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

