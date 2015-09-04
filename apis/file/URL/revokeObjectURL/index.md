---
title: revokeObjectURL
tags:
  0: API
  1: Object
  2: Methods
  4: FileAPI
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
notes:
  - 'Needs example'
summary: 'Revokes a URL from a document and frees the object associated with that URL.'
uri: apis/file/URL/revokeObjectURL

---
# revokeObjectURL

## Summary

Revokes a URL from a document and frees the object associated with that URL.

*Method of [apis/file/URL](/apis/file/URL)*

## Syntax

``` {.js}
 URL.revokeObjectURL(objectURL);
```

## Parameters

### objectURL

 Data-typeÂ
:   String

 String that indicates the URL to revoke from the document.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

This method does not need to be called on a URL object that was created using *oneTimeOnly* set to true. If a URL object is created and not used, this method must be called to revoke it. All URLs that are not revoked will be destroyed when the markup that created them is torn down.

## Related specifications

Specification
:   Status
[W3C File API Specification](http://www.w3.org/TR/FileAPI)
:   W3C Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [Windows Internet Explorer API reference Article](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx)

