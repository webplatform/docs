---
title: ondownloading
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/appcache/ApplicationCache
    href: /apis/appcache/ApplicationCache
  return:
    predicate: 'Returns an object of type '
    value: 'null'
    href: /apis/appcache/ApplicationCache
standardization_status: 'W3C Editor''s Draft'
summary: 'The user agent has found an update and is fetching it, or is downloading the resources listed by the manifest for the first time.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/ondownloading

---
## <span>Summary</span>

The user agent has found an update and is fetching it, or is downloading the resources listed by the manifest for the first time.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## <span>Syntax</span>

``` js
var result = window.applicationCache.ondownloading;
window.applicationCache.ondownloading = value;
```

## <span>Return Value</span>

Returns an object of type nullnull

**Needs Examples**: This section should include examples.

## <span>Notes</span>

If more than one event is triggered and the **downloading** event is included, the next events may include **progress**, **error**, **cached**, or **updateready**. Alternatively, you could use an anonymous delegate function such as

    object.ondownloading = function (e) { … }

where e is the cached event.

## <span>Related specifications</span>

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
