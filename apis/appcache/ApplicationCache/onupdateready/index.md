---
title: onupdateready
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
summary: 'The ApplicationCache object''s cache host is associated with an application cache whose application cache group''s update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/onupdateready

---
## Summary

The ApplicationCache object's cache host is associated with an application cache whose application cache group's update status is idle, and whose application cache group is not marked as obsolete, but that application cache is not the newest cache in its group.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## Syntax

``` js
var result = window.applicationCache.onupdateready;
window.applicationCache.onupdateready = value;
```

## Return Value

Returns an object of type nullnull

## Examples

Checking fo the updateready status

``` js
// try to trigger an application cache update
window.applicationCache.update();

if (window.applicationCache.status === window.applicationCache.UPDATEREADY) {
   console.log('Cache is now ready for an update');
   // now you can call the swapCache() method to switch to the new cache
   window.applicationCache.swapCache();
}
```

Listening for updateready events

``` js
window.applicationCache.addEventListener('updateready',function () {
  console.log('The manifest update download has been completed successfully');
}, false);
```

## Notes

If this event indicates that the resources have been redownloaded, the script can use [swapCache](/apis/appcache/ApplicationCache/swapCache) to switch to the new cache. If there is more than one event, the **updateready** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.onupdateready = function (e) { … }

where e is the cached event.

## Related specifications

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
