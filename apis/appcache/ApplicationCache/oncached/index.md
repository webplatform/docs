---
title: oncached
tags:
  - API
  - Object
  - Properties
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'The resources listed in the manifest have been downloaded, and the application is now cached.'
uri: apis/appcache/ApplicationCache/oncached

---
# oncached

## Summary

The resources listed in the manifest have been downloaded, and the application is now cached.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)</span></span>

## Syntax

``` {.js}
var result = window.applicationCache.oncached;
window.applicationCache.oncached = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">null</span></span>

**Needs Examples**: This section should include examples.

## Notes

If there is more than one event, the **cached** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.oncached = function (e) { … }

where e is the cached event.

## Related specifications

Specification
:   Status
[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

