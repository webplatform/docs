---
title: 'revokeObjectURL'
attributions:
  - 'Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)'
notes:
  - 'Needs example'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: apis/file/URL
    href: /apis/file/URL
standardization_status: 'W3C Working Draft'
summary: 'Revokes a URL from a document and frees the object associated with that URL.'
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
uri: apis/file/URL/revokeObjectURL

---
## Summary

Revokes a URL from a document and frees the object associated with that URL.

Method of [apis/file/URL](/apis/file/URL)[apis/file/URL](/apis/file/URL)

## Syntax

``` js
 URL.revokeObjectURL(objectURL);
```

## Parameters

### objectURL

 Data-type
:   String

 String that indicates the URL to revoke from the document.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

This method does not need to be called on a URL object that was created using *oneTimeOnly* set to true. If a URL object is created and not used, this method must be called to revoke it. All URLs that are not revoked will be destroyed when the markup that created them is torn down.

## Related specifications

[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft
