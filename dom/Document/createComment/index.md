---
title: createComment
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: "Creates a comment object\_with the specified data."
uri: dom/Document/createComment

---
# createComment

## Summary

Creates a comment objectÂ with the specified data.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var commentNode = document.createComment(text);
```

## Parameters

### text

 Data-typeÂ
:   String

 Text of the comment.

## Return Value

Returns an object of type DOM Node.

The created comment node.

## Examples

``` {.js}
//create a comment node
var cmt = document.createComment("Comment text");
//add the comment to the document body
document.body.appendChild(cmt);
```

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

