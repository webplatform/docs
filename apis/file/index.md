---
title: file
tags:
  0: API
  1: Listings
  3: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'The File API allows a developer to use javascript to access the contents and local path of a file uploaded from the input file widget. This enables the developer to build a javascript frontend that allows the website to show a preview of the file uploaded. By using the File API, the developer can also enable a user to upload files via drag-and-drop. Prior to the File API, functionalities like these can only be accomplished via Flash or other plugins.'
uri: apis/file

---
# file

## Summary

The File API allows a developer to use javascript to access the contents and local path of a file uploaded from the input file widget. This enables the developer to build a javascript frontend that allows the website to show a preview of the file uploaded. By using the File API, the developer can also enable a user to upload files via drag-and-drop. Prior to the File API, functionalities like these can only be accomplished via Flash or other plugins.

API Name
:   Summary
[Blob](/apis/file/Blob)
:   The **Blob** object represents immutable raw data. It provides a method to slice data objects between ranges of bytes into further chunks of raw data.
[File](/apis/file/File)
:   The **File** object provides information about files stored on the user's computer, and access to their contents. These are generally retrieved from a [FileList](/apis/file/FileList) object returned when a user selects files using the **input** element, or from a drag-and-drop operation's **DataTransfer** object.
[FileError](/apis/file/FileError)
:   Represents an error that occurs while using the FileReader interface.

    Obsolete per latest specification. Use [DOMError](/dom/DOMError) instead.

[FileList](/apis/file/FileList)
:   FileList is an object which represents an array of individually selected files from the underlying system.
[FileReader](/apis/file/FileReader)
:   The **FileReader** object lets web applications asynchronously read the contents of files (or raw data buffers) stored on the user's computer, using File or Blob objects to specify the file or data to read. File objects may be obtained from a FileList object returned as a result of a user selecting files using the *input* element, from a drag-and-drop operation's *DataTransfer* object, or from the *mozGetAsFile() API* on an *HTMLCanvasElement*.
[FileReaderSync](/apis/file/FileReaderSync)
:   Allows for synchronous reading of File or Blob objects. Only available in Workers, as synchronous I/O would otherwise block the main application from executing.
[MSStreamError](/apis/file/MSStreamError)
:   The MSStreamError object reports file-related errors asynchronously.

    Obsolete per latest specification. Use [DOMError](/dom/DOMError) instead.

[MSStreamReader](/apis/file/MSStreamReader)
:   Creates random access data (Blob) from an MSStream object.
[ObjectURLOptions](/apis/file/ObjectURLOptions)
:   Provides the *oneTimeOnly* property for use with the *createObjectURL* method.
[URL](/apis/file/URL)
:   A static object for URL related utility operations.

## See also

### Related articles

#### Off-line Storage

-   [appcache](/apis/appcache)

-   [status](/apis/appcache/ApplicationCache/status)

-   **file**

-   [File System API](/apis/filesystem)

-   [quota management](/apis/quota_management)

-   [StorageQuota](/apis/quota_management/StorageQuota)

-   [queryUsageAndQuota](/apis/quota_management/queryUsageAndQuota)

-   [requestQuota](/apis/quota_management/requestQuota)

-   [localStorage](/apis/web-storage/Storage/localStorage)

-   [Introduction to using the application cache](/tutorials/appcache_beginner)

-   [Overview of client-side storage](/tutorials/offline_storage)

