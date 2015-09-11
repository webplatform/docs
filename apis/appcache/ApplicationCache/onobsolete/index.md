---
title: onobsolete
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
summary: 'The Webpage is associated with an application cache whose group is marked as obsolete.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/onobsolete

---
## <span>Summary</span>

The Webpage is associated with an application cache whose group is marked as obsolete.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## <span>Syntax</span>

``` js
var result = window.applicationCache.onobsolete;
window.applicationCache.onobsolete = value;
```

## <span>Return Value</span>

Returns an object of type nullnull

## <span>Examples</span>

Checking fo the obsolete status

``` js
// try to trigger an application cache update
window.applicationCache.update();

// Asking the server for the manifest file returned status 404 or 410
// (results in appcache beeing deleted)
if (window.applicationCache.status === window.applicationCache.OBSOLETE) {
   console.log('The cache manifest is gone!');
}
```

Listening for obsolete events

``` js
window.applicationCache.addEventListener('obsolete',function () {
   console.log('The cache manifest is gone!');
}, false);
```

## <span>Notes</span>

If the manifest file can't be found, the cache is considered to be deleted. If there is more than one event, the **obsolete** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.onobsolete = function (e) { … }

where e is the cached event.