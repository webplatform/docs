---
title: createRange
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Creates an empty Range instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.'
uri: dom/Document/createRange

---
# createRange

## Summary

Creates an empty Range instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var range = document.createRange();
```

## Return Value

Returns an object of type DOM Node.

An empty [**Range**](/dom/Range) instance object.

## Examples

``` {.js}
//create a document range
var myRange = document.createRange();
//set starting and ending boundaries using predefined objects and variables
myRange.setStart(startNode, startOffset);
myRange.setEnd(endNode, endOffset);
```

## Related specifications

Specification
:   Status
[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level-2-Range-Creating)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/Document.createRange)

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

