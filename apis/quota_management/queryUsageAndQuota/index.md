---
title: 'queryUsageAndQuota'
notes:
  - 'Can''t find this method in the spec: https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/quota_management/StorageQuota
    href: /apis/quota_management/StorageQuota
standardization_status: 'W3C Editor''s Draft'
summary: 'Queries the current usage (how much data is stored) and quota available for the requesting application.'
tags:
  - API_Object_Methods
  - API
  - Quota_Management
  - Needs_Examples
uri: 'apis/quota management/queryUsageAndQuota'

---
## Summary

Queries the current usage (how much data is stored) and quota available for the requesting application.

Method of [apis/quota\_management/StorageQuota](/apis/quota_management/StorageQuota)[apis/quota\_management/StorageQuota](/apis/quota_management/StorageQuota)

## Syntax

``` js
 object.queryUsageAndQuota(/* see parameter list */);
```

## Parameters

### successCallback

 Data-type
:   String

 This callback is used to return new quota information granted by a User Agent. Quota is provided by the *grantedQuotaInBytes* parameter.

**void (unsigned long grantedQuotaInBytes)**

### errorCallback

 Data-type
:   String

 This callback is used to return information when an error has occured. Details are provided by the *error* parameter.

**void (DOMError error)**

## Return Value

No return value

## Related specifications

[W3C Quota Management Specification](https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html)
:   W3C Editor's Draft

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   **queryUsageAndQuota**

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
