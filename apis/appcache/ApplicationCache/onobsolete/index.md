---
title: onobsolete
tags:
  - API
  - Object
  - Properties
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'The Webpage is associated with an application cache whose group is marked as obsolete.'
uri: apis/appcache/ApplicationCache/onobsolete

---
# onobsolete

## Summary

The Webpage is associated with an application cache whose group is marked as obsolete.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)</span></span>

## Syntax

``` {.js}
var result = window.applicationCache.onobsolete;
window.applicationCache.onobsolete = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">null</span></span>

## Examples

Checking fo the obsolete status

``` {.js}
// try to trigger an application cache update
window.applicationCache.update();

// Asking the server for the manifest file returned status 404 or 410
// (results in appcache beeing deleted)
if (window.applicationCache.status === window.applicationCache.OBSOLETE) {
   console.log('The cache manifest is gone!');
}
```

Listening for obsolete events

``` {.js}
window.applicationCache.addEventListener('obsolete',function () {
   console.log('The cache manifest is gone!');
}, false);
```

## Notes

If the manifest file can't be found, the cache is considered to be deleted. If there is more than one event, the **obsolete** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.onobsolete = function (e) { … }

where e is the cached event.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

