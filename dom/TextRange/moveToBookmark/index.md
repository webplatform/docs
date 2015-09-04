---
title: moveToBookmark
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: Non-Standard
notes:
  - 'needs example'
summary: 'Moves to a bookmark.'
uri: dom/TextRange/moveToBookmark

---
# moveToBookmark

## Summary

Moves to a bookmark.

*Method of [dom/TextRange](/dom/TextRange)*

## Syntax

``` {.js}
var result = textRange.moveToBookmark(/* see parameter list */);
```

## Parameters

### Bookmark

 Data-typeÂ
:   BSTR

**String**Â that specifies the bookmark to move to.

## Return Value

Returns an object of type Boolean.

Boolean

**Boolean** that returns one of the following possible values:

Return value
:   Description
true
:   Successfully moved to the bookmark.
false
:   Move to the bookmark failed.

Â

**Needs Examples**: This section should include examples.

## Notes

### Remarks

Bookmarks are opaque strings created with the [**getBookmark**](/dom/TextRange/getBookmark) method. This feature might not be available on non-Microsoft Win32 platforms.

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[moveToBookmark Method](http://msdn.microsoft.com/en-us/library/ie/ms536628(v=vs.85).aspx) Article]

