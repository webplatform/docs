---
title: 'onnoupdate'
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
summary: 'Indicates the manifest has not changed.'
tags:
  - API_Object_Properties
  - Appcache
  - API
uri: apis/appcache/ApplicationCache/onnoupdate

---
## Summary

Indicates the manifest has not changed.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## Syntax

``` js
var result = window.applicationCache.onnoupdate;
window.applicationCache.onnoupdate = value;
```

## Return Value

Returns an object of type nullnull

## Examples

If the currently-cached copy of the manifest is up-to-date, the browser sends a noupdate event to the applicationCache object, and the update process is complete. Note that if you change any cached resources on the server, you must also change the manifest file itself, so that the browser knows it needs to fetch all the resources again.

``` js
window.applicationCache.addEventListener('noupdate',function () {
  console.log('The manifest file is up to date');
}, false);
```

## Notes

If there is more than one event, the **onupdate** event will be the last one in the sequence. Alternatively, you could use an anonymous delegate function such as

    object.onnoupdate = function (e) { … }

where e is the cached event.
