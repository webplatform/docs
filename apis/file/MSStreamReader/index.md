---
title: 'MSStreamReader'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
standardization_status: Non-Standard
summary: 'Creates random access data (Blob) from an MSStream object.'
tags:
  - API_Objects
  - API
  - FileAPI
  - Needs_Examples
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/MSStream
uri: apis/file/MSStreamReader

---
## Summary

Creates random access data (Blob) from an MSStream object.

## Properties

[onabort](/apis/file/MSStreamReader/onabort)
:   Indicates that the read has been aborted (for example, by calling **abort()**).

## Methods

[readAsBlob](/apis/file/MSStreamReader/readAsBlob)
:   Performs an asynchronous read of an [MSStream](/w/index.php?title=apis/file/MSStream&action=edit&redlink=1) object in order to create a [Blob](/apis/file/Blob) object.

[readAsText](/apis/file/MSStreamReader/readAsText)
:   Returns partial Blob data representing the number of bytes currently loaded (as a fraction of the total), decoded into memory according to the encoding determination.

## Events

*No events.*

## Notes

**MSStreamReader** is a constructor function producing an object that provides methods to asynchronously read an [MSStream](/w/index.php?title=apis/file/MSStream&action=edit&redlink=1), and an event model to obtain the results of these reads. MSStreamReader lets you read and interact with MSStream objects. MSStreamReader performs the conversion of multimedia that is in a C++ file format into a format that can be accessed by JavaScript. The original file is accessed as an MSStream that overlays a Blob object. MSStreamReader uses the *readAsBlob* method to perform an asynchronous read of data from the MSStream when converting it to a Blob. A series of events is used to track the progress of the read and any errors that occur. The MSStreamReader can be in one of three states. The *readyState* returns the current state. The state is one of the following values:

-   EMPTY. The MSStreamReader object has been created and there are no pending reads. This is the default state of a new MSStreamReader object until the *readAsBlob* method is called.
-   LOADING. An MSStream is being read. The *readAsBlob* method is running and no error has occurred during the read.
-   DONE. The entire MSStream has been read into memory, a file error occurred during the read, or the read was aborted using the *abort* method. The MSStreamReader is no longer reading an MSStream. If *readyState* is set to `DONE`, it means that the *readAsBlob* method has been called at least once.

When the MSStreamReader read operation is done on the MSStream, the *result* property returns the Blob object that contains the data buffered from the MSStream. The *result* is returned after the *onloadend* event has fired.
