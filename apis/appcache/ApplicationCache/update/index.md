---
title: update
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/appcache/ApplicationCache
    href: /apis/appcache/ApplicationCache
  return_type:
    predicate: 'Returns an object of type  '
    value: 'null'
    href: /apis/appcache/ApplicationCache
standardization_status: 'W3C Editor''s Draft'
summary: 'Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.'
tags:
  - API
  - Object
  - Methods
  - Appcache
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/appcache/properties/status
    - apis/appcache/methods/swapCache
uri: apis/appcache/ApplicationCache/update

---
## <span>Summary</span>

Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.

Method of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## <span>Syntax</span>

``` js
var result = window.applicationCache.update();
```

## <span>Return Value</span>

Returns an object of type nullnull

Type: **HRESULT**

This method can return one of these values.

<table>
<col width="50%" />
<col width="50%" />
<thead>
<tr class="header">
<th align="left">Return code/value</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">S_OK</td>
<td align="left"></td>
</tr>
<tr class="even">
<td align="left">DOMException.INVALID_STATE_ERR
<p>11</p></td>
<td align="left">This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.</td>
</tr>
</tbody>
</table>

## <span>Examples</span>

``` js
var applicationCache = window.applicationCache;



applicationCache.update();  // Attempt to update the user's cache.

if (applicationCache.status == window.applicationCache.UPDATEREADY) {

    applicationCache.swapCache();  // The fetch was successful, switch to the new cache.

        if (confirm('A new version of this site is available. Do you want to load it?')) {

            window.location.reload();

        }

}
```

## <span>Notes</span>

Use this method and check the [status](/w/index.php?title=apis/appcache/properties/status&action=edit&redlink=1) before using [swapCache](/w/index.php?title=apis/appcache/methods/swapCache&action=edit&redlink=1).

The **update** method returns before the update check is complete, so it is a best practice to wait before checking the [status](/w/index.php?title=apis/appcache/properties/status&action=edit&redlink=1) property or calling the [swapCache](/w/index.php?title=apis/appcache/methods/swapCache&action=edit&redlink=1) method.

The **update** method is provided for convenience, but is not necessary for basic functionality. Loading or refreshing the page is sufficient.

## <span>Related specifications</span>

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
