---
title: status
attributions:
  - 'Microsoft Developer Network: [Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
  - 'Portions of this content come from HTML5Rocks! [article](http://www.html5rocks.com/en/tutorials/appcache/beginner/)'
relationships:
  applies_to:
    predicate: 'Property of '
    value: apis/appcache/ApplicationCache
    href: /apis/appcache/ApplicationCache
  return:
    predicate: 'Returns an object of type '
    value: 'unsigned short'
    href: /apis/appcache/ApplicationCache
standardization_status: 'W3C Editor''s Draft'
summary: 'Returns the current status of the application cache, as given by the constants defined below.'
tags:
  - API
  - Object
  - Properties
  - Appcache
uri: apis/appcache/ApplicationCache/status

---
## Summary

Returns the current status of the application cache, as given by the constants defined below.

Property of [apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)[apis/appcache/ApplicationCache](/apis/appcache/ApplicationCache)

## Syntax

**Note**: This property is read-only.

``` js
var result = ApplicationCache.status;
```

## Return Value

Returns an object of type unsigned shortunsigned short

**UNCACHED** (numeric value 0)
:   The current webpage doesn't use an application cache at this time.

**IDLE** (numeric value 1)
:   The current webpage's application cache is the newest available, it's content is not being updated or marked as obsolete.

**CHECKING** (numeric value 2)
:   The current webpage's application cache is checking for an update.

**DOWNLOADING** (numeric value 3)
:   An update for the cached resources was found and is now being downloaded.

**UPDATEREADY** (numeric value 4)
:   The updated ressources have been newly redownloaded.

**OBSOLETE** (numeric value 5)
:   The current webpage's application cache is marked as obsolete.

## Examples

``` js
var appCache = window.applicationCache;

switch (appCache.status) {
  case appCache.UNCACHED: // UNCACHED == 0
    return 'UNCACHED';
    break;
  case appCache.IDLE: // IDLE == 1
    return 'IDLE';
    break;
  case appCache.CHECKING: // CHECKING == 2
    return 'CHECKING';
    break;
  case appCache.DOWNLOADING: // DOWNLOADING == 3
    return 'DOWNLOADING';
    break;
  case appCache.UPDATEREADY:  // UPDATEREADY == 4
    return 'UPDATEREADY';
    break;
  case appCache.OBSOLETE: // OBSOLETE == 5
    return 'OBSOLETE';
    break;
  default:
    return 'UKNOWN CACHE STATUS';
    break;
};
```

## Related specifications

[W3C ApplicationCache Specification](http://dev.w3.org/html5/spec/single-page.html#dom-appcache-status)
:   W3C Editor's Draft

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   **status**

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [StorageQuota](/apis/quota_management/StorageQuota)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
