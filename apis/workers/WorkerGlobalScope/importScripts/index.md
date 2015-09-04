---
title: importScripts
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
readiness: 'Almost Ready'
standardization_status: 'W3C Editor''s Draft'
notes:
  - 'Needs example'
summary: 'Fetches one or more script resources, identified by absolute URLs.'
uri: apis/workers/WorkerGlobalScope/importScripts

---
# importScripts

## Summary

Fetches one or more script resources, identified by absolute URLs.

*Method of [apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)*

## Syntax

``` {.js}
 object.importScripts(urls);
```

## Parameters

### urls

 Data-typeÂ
:   String

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

A URL that is loaded must resolve according to the **WorkerLocation** of the worker. More than one script can be loaded in a sequence of URLs. The loading and executing of scripts is synchronous. If any script throws an exception, subsequent scripts will not load.

## Related specifications

Specification
:   Status
[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

