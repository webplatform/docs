---
title: 'StorageQuota'
notes:
  - "Missing supportedTypes attribute (https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html#widl-StorageQuota-supportedTypes).\nThe methods in the spec differ from the two listed here. The spec has:\nqueryInfo\n\nrequestPersistentQuota"
readiness: 'Not Ready'
standardization_status: 'W3C Editor''s Draft'
summary: 'Provides a means to query and request storage usage and quota information.'
tags:
  - API_Objects
  - API
  - Quota_Management
  - Needs_Examples
uri: 'apis/quota management/StorageQuota'

---
## Summary

Provides a means to query and request storage usage and quota information.

## Properties

*No properties.*

## Methods

[queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)
:   Queries the current usage (how much data is stored) and quota available for the requesting application.

[requestQuota](/apis/quota_management/requestQuota)
:   Requests a new quota for the requesting application.

## Events

*No events.*

## Related specifications

[W3C Quota Management Specification](https://dvcs.w3.org/hg/quota/raw-file/tip/Overview.html#storagequota-interface)
:   W3C Editor's Draft

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
