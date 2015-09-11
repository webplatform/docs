---
title: navigator
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
    value: Object
    href: /apis/workers/WorkerGlobalScope
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns an instance of the WorkerNavigator interface, which represents the identity and state of the user agent (the client).'
tags:
  0: API
  1: Object
  2: Properties
  4: Webworkers
uri: apis/workers/WorkerGlobalScope/navigator

---
## <span>Summary</span>

Returns an instance of the WorkerNavigator interface, which represents the identity and state of the user agent (the client).

Property of [apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)[apis/workers/WorkerGlobalScope](/apis/workers/WorkerGlobalScope)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var result = object.navigator;
```

## <span>Return Value</span>

Returns an object of type ObjectObject

**Needs Examples**: This section should include examples.

## <span>Notes</span>

The **WorkerNavigator** object returned by this property can provide information about the browser a worker is running in.

## <span>Related specifications</span>

[W3C Web Workers Specification](http://dev.w3.org/html5/workers)
:   W3C Editor's Draft
