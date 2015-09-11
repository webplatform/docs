---
title: requestQuota
notes:
  - 'Can''t find this method in the spec: https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: 'apis/quota management/StorageQuota'
    href: /apis/quota_management/StorageQuota
standardization_status: 'W3C Working Draft'
summary: 'Requests a new quota for the requesting application.'
tags:
  0: API
  1: Object
  2: Methods
  4: Quota
  5: Management
uri: 'apis/quota management/requestQuota'

---
## <span>Summary</span>

Requests a new quota for the requesting application.

Method of [apis/quota management/StorageQuota](/apis/quota_management/StorageQuota)[apis/quota management/StorageQuota](/apis/quota_management/StorageQuota)

## <span>Syntax</span>

``` js
 object.requestQuota(/* see parameter list */);
```

## <span>Parameters</span>

### <span>newQuotaInBytes</span>

 Data-type
:   unsigned long

 The requested new quota, expressed in bytes.

### <span>successCallback</span>

 Data-type
:   String

(Optional)

This callback is used to return new quota information granted by a User Agent. Quota is provided by the *grantedQuotaInBytes* parameter.

**void (unsigned long grantedQuotaInBytes)**

### <span>errorCallback</span>

 Data-type
:   String

(Optional)

This callback is used to return information when an error has occured. Details are provided by the *error* parameter.

**void (DOMError error)**

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Notes</span>

It is not guaranteed that the requested amount of space is granted just by calling this API. Calling this API may trigger user prompting to request explicit user permission to proceed. The successCallback callback may return a smaller amount of quota than requested.

## <span>Related specifications</span>

[W3C Quota Management API](http://www.w3.org/TR/quota-api/)
:   W3C Working Draft

## <span>See also</span>

### <span>Related articles</span>

#### <span>Off-line Storage</span>

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   **requestQuota**

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
