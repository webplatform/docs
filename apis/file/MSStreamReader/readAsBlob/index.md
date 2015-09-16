---
title: readAsBlob
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Non-standard; deletion candidate'
readiness: 'Not Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/MSStreamReader
    href: /apis/file/MSStreamReader
standardization_status: Non-Standard
summary: 'Performs an asynchronous read of an MSStream object in order to create a Blob object.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - apis/file/MSStream
uri: apis/file/MSStreamReader/readAsBlob

---
## Summary

Performs an asynchronous read of an MSStream object in order to create a Blob object.

Method of [apis/file/MSStreamReader](/apis/file/MSStreamReader)[apis/file/MSStreamReader](/apis/file/MSStreamReader)

## Syntax

``` js
 MSStreamReader.readAsBlob(/* see parameter list */);
```

## Parameters

### stream

 Data-type
:   Blob

 The [MSStream](/w/index.php?title=apis/file/MSStream&action=edit&redlink=1) object to read.

### maxSize

 Data-type
:   Number

(Optional)

String that specifies the maximum size of the object to read.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

The **readAsBlob** method is used by [msStreamReader](/apis/file/MSStreamReader) to create a [Blob](/apis/file/Blob) object from an [MSStream](/w/index.php?title=apis/file/MSStream&action=edit&redlink=1). When the read begins, the *readyState* property is set to the `LOADING` state on MSStreamReader and the *onloadstart* event is fired. Progress for the read is monitored by the *onprogress* event. When the read completes, the *onloadend* event fires and *readyState* is set to `DONE` and *MSStreamReader.result* returns the new Blob object. A read operation can be interrupted if an error occurs or the *abort* method is run. If an error occurs, the *onloadend* event sets the *readyState* to `DONE`, and passes the error using the *error* property.
