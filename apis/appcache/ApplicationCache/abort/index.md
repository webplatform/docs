---
title: abort
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Add example, notes section.'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/appcache/ApplicationCache
    href: /apis/appcache/ApplicationCache
standardization_status: 'W3C Editor''s Draft'
summary: 'Cancels the application cache download process. This method is intended to be used by Web applications showing their own caching progress UI, in case the user wants to stop the update (e.g., because bandwidth is limited).'
tags:
  - API
  - Object
  - Methods
  - Appcache
uri: apis/appcache/ApplicationCache/abort

---
## <span>Summary</span>

Cancels the application cache download process. This method is intended to be used by Web applications showing their own caching progress UI, in case the user wants to stop the update (e.g., because bandwidth is limited).

Method of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## <span>Syntax</span>

``` js
 window.applicationCache.abort();
```

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Related specifications</span>

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
