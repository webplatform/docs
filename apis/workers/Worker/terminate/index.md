---
title: terminate
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs example'
summary: 'Immediately terminates the worker with which the object is associated.'
uri: apis/workers/Worker/terminate

---
# terminate

## Summary

Immediately terminates the worker with which the object is associated.

*Method of [apis/workers/Worker](/apis/workers/Worker)*

## Syntax

``` {.js}
 object.terminate();
```

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

You can terminate a worker thread inside its own code by using the **self.close()** method.

## Related specifications

Specification
:   Status
[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

