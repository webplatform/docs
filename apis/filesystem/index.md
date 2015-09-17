---
title: 'File System API'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
summary: "The File System API simulates a local file system that web apps can navigate around. You can develop apps that can read, write, and create files and directories in a virtual, sandboxed file system. The asynchronous API methods return without blocking the calling thread. The asynchronous API doesn't give you data by returning values; instead, you have to pass a callback function. The synchronous API is intended to be used with WebWorkers.\n"
tags:
  - API_Listings
  - API
  - FileSystemAPI
uri: apis/filesystem

---
## Summary

The File System API simulates a local file system that web apps can navigate around. You can develop apps that can read, write, and create files and directories in a virtual, sandboxed file system. The asynchronous API methods return without blocking the calling thread. The asynchronous API doesn't give you data by returning values; instead, you have to pass a callback function. The synchronous API is intended to be used with WebWorkers.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[DirectoryEntry](/apis/filesystem/DirectoryEntry)
:   This interface represents a directory on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[DirectoryReader](/apis/filesystem/DirectoryReader)
:   This interface lets a user list files and directories in a directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileEntry](/apis/filesystem/FileEntry)
:   This interface represents a file on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileSystem](/apis/filesystem/FileSystem)
:   In the File System API, a FileSystem object represents a file system. The object is the argument of a successful callback of requestFileSystem().

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileSystemSync](/apis/filesystem/FileSystemSync)
:   In the File System API, a FileSystemSync object represents a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   **File System API**

-   [quota management](/apis/quota_management)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)
