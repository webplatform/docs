---
title: update
tags:
  - API
  - Object
  - Methods
  - Appcache
standardization_status: 'W3C Editor''s Draft'
summary: 'Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.'
uri: apis/appcache/ApplicationCache/update
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/appcache/properties/status
    - apis/appcache/methods/swapCache

---
# update

## Summary

Invokes the application cache download process. Throws an InvalidStateError exception if there is no application cache to update. Calling this method is not usually necessary, as user agents will generally take care of updating application caches automatically. The method can be useful in situations such as long-lived applications. For example, a Web mail application might stay open in a browser tab for weeks at a time. Such an application could want to test for updates each day.

*Method of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)*

## Syntax

``` {.js}
var result = window.applicationCache.update();
```

## Return Value

Returns an object of type null.

Type: **HRESULT**

This method can return one of these values.

<dl data-table="wikitable">
<dt>
Return code/value

</dt>
<dd>
Description

</dd>
<dt>
S\_OK

</dt>
<dd>
</dd>
<dt>
DOMException.INVALID\_STATE\_ERR

11

</dt>
<dd>
This exception is thrown if the application cache cannot be found or the status of the cache is obsolete.

</dd>
</dl>
## Examples

``` {.js}
var applicationCache = window.applicationCache;



applicationCache.update();  // Attempt to update the user's cache.

if (applicationCache.status == window.applicationCache.UPDATEREADY) {

    applicationCache.swapCache();  // The fetch was successful, switch to the new cache.

        if (confirm('A new version of this site is available. Do you want to load it?')) {

            window.location.reload();

        }

}
```

## Notes

Use this method and check the [status](/w/index.php?title=apis/appcache/properties/status&action=edit&redlink=1) before using [swapCache](/w/index.php?title=apis/appcache/methods/swapCache&action=edit&redlink=1).

The **update** method returns before the update check is complete, so it is a best practice to wait before checking the [status](/w/index.php?title=apis/appcache/properties/status&action=edit&redlink=1) property or calling the [swapCache](/w/index.php?title=apis/appcache/methods/swapCache&action=edit&redlink=1) method.

The **update** method is provided for convenience, but is not necessary for basic functionality. Loading or refreshing the page is sufficient.

## Related specifications

Specification
:   Status
[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

