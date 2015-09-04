---
title: onchecking
tags:
  - API
  - Object
  - Properties
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'The user agent is checking for an update, or attempting to download the manifest for the first time. This is always the first event in the sequence.'
uri: apis/appcache/ApplicationCache/onchecking

---
# onchecking

## Summary

The user agent is checking for an update, or attempting to download the manifest for the first time. This is always the first event in the sequence.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)</span></span>

## Syntax

``` {.js}
var result = window.applicationCache.onchecking;
window.applicationCache.onchecking = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">null</span></span>

**Needs Examples**: This section should include examples.

## Notes

If more than one event is triggered and the **checking** event is included, the next events may include **noupdate**, **downloading**, **obsolete**, or **error**. Alternatively, you could use an anonymous delegate function such as

    object.onchecking = function (e) { … }

where e is the cached event.

## Related specifications

Specification
:   Status
[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

