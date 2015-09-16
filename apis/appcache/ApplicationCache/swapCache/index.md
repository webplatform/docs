---
title: 'swapCache'
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/appcache/beginner/)'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/appcache/ApplicationCache
    href: /apis/appcache/ApplicationCache
standardization_status: 'W3C Editor''s Draft'
summary: "Switches to the most recent application cache, if there is a newer one. If there isn't, throws an InvalidStateError exception.\n"
tags:
  - API
  - Object
  - Methods
  - Appcache
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/appcache/methods/update
uri: apis/appcache/ApplicationCache/swapCache

---
## Summary

Switches to the most recent application cache, if there is a newer one. If there isn't, throws an InvalidStateError exception.

This does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.

The **updateready** event will fire before this method can be called. Once it fires, the Web application can, at its leisure, call this method to switch the underlying cache to the one with the more recent updates. To make proper use of this, applications have to be able to bring the new features into play; for example, reloading scripts to enable new features. An easier alternative to `swapCache()` is just to reload the entire page at a time suitable for the user, using `location.reload()`.

Method of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## Syntax

``` js
 window.applicationCache.swapCache();
```

## Return Value

No return value

## Examples

``` js
// Attempt to update the user's cache.
window.applicationCache.update();

…

if (window.applicationCache.status === window.applicationCache.UPDATEREADY) {
  // The fetch was successful, swap in the new cache.
  window.applicationCache.swapCache();
}
```

## Usage

     In order to swap an old cache out for a new one, call update first. When the status is in the UPDATEREADY state, calling swapCache will make the swap.

Calling **swapCache** will not update any content on your page. It will simply allow your webpage to be able to access any further dynamic content from the new cache instead of the old one. After the page is refreshed, the newly created cache will be used for all in-page and dynamic requests. The **swapCache** method is provided for convenience but is not necessary for basic functionality. Loading or refreshing the page is sufficient. For example, refreshing the page after an **UpdateReady** event will reload the page from the new cache without a call to **swapCache**.

**swapCache** does not cause previously-loaded resources to be reloaded; for example, images do not suddenly get reloaded, and style sheets and scripts do not get reparsed or reevaluated. The only change is that subsequent requests for cached resources will obtain the newer copies.

## Related specifications

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#application-cache-api)
:   W3C Editor's Draft
