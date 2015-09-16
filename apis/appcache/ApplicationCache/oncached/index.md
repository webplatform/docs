---
title: oncached
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
summary: 'The resources listed in the manifest have been downloaded, and the application is now cached.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/oncached

---
## Summary

The resources listed in the manifest have been downloaded, and the application is now cached.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## Syntax

``` js
var result = window.applicationCache.oncached;
window.applicationCache.oncached = value;
```

## Return Value

Returns an object of type nullnull

**Needs Examples**: This section should include examples.

## Notes

If there is more than one event, the **cached** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.oncached = function (e) { … }

where e is the cached event.

## Related specifications

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
