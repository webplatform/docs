---
title: onprogress
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
summary: 'The user agent is downloading resources listed by the manifest. The event object''s total attribute returns the total number of files to be downloaded. The event object''s loaded attribute returns the number of files processed so far.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/onprogress

---
## <span>Summary</span>

The user agent is downloading resources listed by the manifest. The event object's total attribute returns the total number of files to be downloaded. The event object's loaded attribute returns the number of files processed so far.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## <span>Syntax</span>

``` js
var result = window.applicationCache.onprogress;
window.applicationCache.onprogress = value;
```

## <span>Return Value</span>

Returns an object of type nullnull

## <span>Examples</span>

Registering an progress event handler to keep track of the number of items that need to be fetched and that are already fetched

``` js
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

## <span>Notes</span>

If more than one event is triggered and the **progress** event is included, the next events may include **progress**, **error**, **cached**, or **updateready**. Alternatively, you could use an anonymous delegate function such as

    object.onprogress = function (e) { … }

where e is the cached event.

## <span>Related specifications</span>

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
