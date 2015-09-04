---
title: FileReaderSync
tags:
  0: API
  1: Objects
  3: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Allows for synchronous reading of File or Blob objects. Only available in Workers, as synchronous I/O would otherwise block the main application from executing.'
uri: apis/file/FileReaderSync

---
# FileReaderSync

## Summary

Allows for synchronous reading of File or Blob objects. Only available in Workers, as synchronous I/O would otherwise block the main application from executing.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Notes

**Important:**  The FileReaderSync object's read methods (readAsText, readAsDataURL, and readAsArrayBuffer) have the same method signatures as the read methods of the [FileReader](/apis/file/FileReader) object but they behave synchronously (as opposed to asynchronously).

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

