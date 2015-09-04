---
title: onprogress
tags:
  - API
  - Object
  - Properties
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'The user agent is downloading resources listed by the manifest. The event object''s total attribute returns the total number of files to be downloaded. The event object''s loaded attribute returns the number of files processed so far.'
uri: apis/appcache/ApplicationCache/onprogress

---
# onprogress

## Summary

The user agent is downloading resources listed by the manifest. The event object's total attribute returns the total number of files to be downloaded. The event object's loaded attribute returns the number of files processed so far.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)</span></span>

## Syntax

``` {.js}
var result = window.applicationCache.onprogress;
window.applicationCache.onprogress = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">null</span></span>

## Examples

Registering an progress event handler to keep track of the number of items that need to be fetched and that are already fetched

``` {.js}
CACHE MANIFEST
# Example manifest
CACHE:
afile.css
anotherfile.js

// will be called two times in total, because there are two files to fetch (afile.css, anotherfile.js)
window.applicationCache.addEventListener('progress', function (event) {
   console.log('Item', event.loaded, 'of', event.total, 'fetched');
}, false);
```

## Notes

If more than one event is triggered and the **progress** event is included, the next events may include **progress**, **error**, **cached**, or **updateready**. Alternatively, you could use an anonymous delegate function such as

    object.onprogress = function (e) { … }

where e is the cached event.

## Related specifications

Specification
:   Status
[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

