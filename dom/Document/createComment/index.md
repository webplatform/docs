---
title: createComment
attributions:
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
summary: "Creates a comment object\_with the specified data."
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createComment

---
## <span>Summary</span>

Creates a comment object with the specified data.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var commentNode = document.createComment(text);
```

## <span>Parameters</span>

### <span>text</span>

 Data-type
:   String

 Text of the comment.

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The created comment node.

## <span>Examples</span>

``` js
//create a comment node
var cmt = document.createComment("Comment text");
//add the comment to the document body
document.body.appendChild(cmt);
```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/)
:   Recommendation
