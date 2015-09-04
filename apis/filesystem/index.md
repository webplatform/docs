---
title: filesystem
tags:
  0: API
  1: Listings
  3: FileSystemAPI
readiness: 'Out of Date'
standardization_status: 'W3C Working Draft'
notes:
  - 'Out of date; feature discontinued. See http://www.w3.org/TR/file-system-api/.'
summary: "The File System API simulates a local file system that web apps can navigate around. You can develop apps that can read, write, and create files and directories in a virtual, sandboxed file system. The asynchronous API methods return without blocking the calling thread. The asynchronous API doesn't give you data by returning values; instead, you have to pass a callback function. The synchronous API is intended to be used with WebWorkers.\n"
uri: apis/filesystem

---
# File System API

## Summary

The File System API simulates a local file system that web apps can navigate around. You can develop apps that can read, write, and create files and directories in a virtual, sandboxed file system. The asynchronous API methods return without blocking the calling thread. The asynchronous API doesn't give you data by returning values; instead, you have to pass a callback function. The synchronous API is intended to be used with WebWorkers.

**Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

API Name
:   Summary
[DirectoryEntry](/apis/filesystem/DirectoryEntry)
:   This interface represents a directory on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[DirectoryEntrySync](/apis/filesystem/DirectoryEntrySync)
:   This interface represents a directory on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[DirectoryReader](/apis/filesystem/DirectoryReader)
:   This interface lets a user list files and directories in a directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[DirectoryReaderSync](/apis/filesystem/DirectoryReaderSync)
:   This interface lets a user list files and directories in a directory.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[EntriesCallback](/apis/filesystem/EntriesCallback)
:   When readEntries() succeeds, this callback is made.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[Entry](/apis/filesystem/Entry)
:   An abstract interface representing entries in a file system, each of which may be a File or DirectoryEntry.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[EntryCallback](/apis/filesystem/EntryCallback)
:   This interface is the callback used to look up Entry objects.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[EntrySync](/apis/filesystem/EntrySync)
:   An abstract interface representing entries in a file system, each of which may be a File or DirectoryEntry.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[ErrorCallback](/apis/filesystem/ErrorCallback)
:   When an error occurs, this callback is made.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileCallback](/apis/filesystem/FileCallback)
:   This interface is the callback used to obtain a File.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileEntry](/apis/filesystem/FileEntry)
:   This interface represents a file on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileEntrySync](/apis/filesystem/FileEntrySync)
:   This interface represents a file on a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileSystem](/apis/filesystem/FileSystem)
:   In the File System API, a FileSystem object represents a file system. The object is the argument of a successful callback of requestFileSystem().

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileSystemCallback](/apis/filesystem/FileSystemCallback)
:   When requestFileSystem() succeeds, this callback is made.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileSystemSync](/apis/filesystem/FileSystemSync)
:   In the File System API, a FileSystemSync object represents a file system.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[FileWriterCallback](/apis/filesystem/FileWriterCallback)
:   This interface is the callback used to create a FileWriter.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[LocalFileSystem](/apis/filesystem/LocalFileSystem)
:   The LocalFileSystem interface of the File System API gives you access to a sandboxed file system. The methods are implemented by window and worker objects.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[LocalFileSystemSync](/apis/filesystem/LocalFileSystemSync)
:   The LocalFileSystemSync interface of the File System API gives you access to a sandboxed file system. It is intended to be used with WebWorkers. The methods are implemented by worker objects.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[MetadataCallback](/apis/filesystem/MetadataCallback)
:   This interface is the callback used to look up file and directory metadata.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

[VoidCallback](/apis/filesystem/VoidCallback)
:   This interface is the generic callback used to indicate success of an asynchronous method.

    **Out of date; feature discontinued. See [http://www.w3.org/TR/file-system-api](http://www.w3.org/TR/file-system-api/).**

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   [file](/apis/file)

-   **File System API**

-   [quota management](/apis/quota_management)

-   [StorageQuota](/apis/quota_management/StorageQuota)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)

-   [Overview of client-side storage](/tutorials/offline_storage)

