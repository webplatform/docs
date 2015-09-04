---
title: onupdateready
tags:
  - API
  - Object
  - Properties
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'The ApplicationCache object''s cache host is associated with an application cache whose application cache group''s update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.'
uri: apis/appcache/ApplicationCache/onupdateready

---
# onupdateready

## Summary

The ApplicationCache object's cache host is associated with an application cache whose application cache group's update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)</span></span>

## Syntax

``` {.js}
var result = window.applicationCache.onupdateready;
window.applicationCache.onupdateready = value;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">null</span></span>

## Examples

Checking fo the updateready status

``` {.js}
// try to trigger an application cache update
window.applicationCache.update();

if (window.applicationCache.status === window.applicationCache.UPDATEREADY) {
   console.log('Cache is now ready for an update');
   // now you can call the swapCache() method to switch to the new cache
   window.applicationCache.swapCache();
}
```

Listening for updateready events

``` {.js}
window.applicationCache.addEventListener('updateready',function () {
  console.log('The manifest update download has been completed successfully');
}, false);
```

## Notes

If this event indicates that the resources have been redownloaded, the script can use [swapCache](/apis/appcache/ApplicationCache/swapCache) to switch to the new cache. If there is more than one event, the **updateready** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.onupdateready = function (e) { … }

where e is the cached event.

## Related specifications

Specification
:   Status
[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

