---
title: close
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/workers/WorkerGlobalScope
    href: /apis/workers/WorkerGlobalScope
standardization_status: 'W3C Editor''s Draft'
summary: 'Discards any pending tasks and immediately closes the worker.'
tags:
  0: API
  1: Object
  2: Methods
  4: Webworkers
uri: apis/workers/WorkerGlobalScope/close

---
## <span>Summary</span>

Discards any pending tasks and immediately closes the worker.

Method of [apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)[apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)

## <span>Syntax</span>

``` js
 object.close();
```

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

This method sets the worker's WorkerGlobalScope object's closing flag to *true*, preventing any further tasks from being queued.

Use the **terminate** method if you want to stop a worker from a parent thread.

## <span>Related specifications</span>

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
