---
title: createRange
attributions:
  - 'Mozilla Developer Network [![cc-by-sa-small-wpd.svg](/assets/thumb/8/8c/cc-by-sa-small-wpd.svg/120px-cc-by-sa-small-wpd.svg.png)](http://creativecommons.org/licenses/by-sa/3.0/us/): [Article](https://developer.mozilla.org/en-US/docs/DOM/Document.createRange)'
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates an empty Range instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createRange

---
## <span>Summary</span>

Creates an empty Range instance object that has both of its boundary points positioned at the beginning of the document. After a Range is created, you must set its starting and ending boundary points before you can make use of most of its methods.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var range = document.createRange();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

An empty [**Range**](/dom/Range) instance object.

## <span>Examples</span>

``` js
//create a document range
var myRange = document.createRange();
//set starting and ending boundaries using predefined objects and variables
myRange.setStart(startNode, startOffset);
myRange.setEnd(endNode, endOffset);
```

## <span>Related specifications</span>

[DOM Level 2 Traversal and Range](http://www.w3.org/TR/DOM-Level-2-Traversal-Range/ranges.html#Level-2-Range-Creating)
:   Recommendation
