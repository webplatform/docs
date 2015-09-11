---
title: document.write
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs examples and compat'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Method to insert a string of marked up text in the document tree.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/write

---
## <span>Summary</span>

Method to insert a string of marked up text in the document tree.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
 document.write(str);
```

## <span>Parameters</span>

### <span>str</span>

 Data-type
:   String

 A **String** that specifies the text and HTML tags to write.

## <span>Return Value</span>

No return value

**Needs Examples**: This section should include examples.

## <span>Usage</span>

     Do not use the write method or the writeln method on the current document after the document has finished loading unless you first call the open method, which clears the current document window and erases all variables.

## <span>Notes</span>

When [**Document**](/dom/Document).**write** or **document**.[**writeln**](/dom/Document/writeln) is used in an event handler, you must also use **document**.[**close**](/dom/Document/close).

## <span>Related specifications</span>

[DOM HTML Level 2](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-75233634)
:   W3C Recommendation

## <span>See also</span>

### <span>Related pages</span>

-   `writeln`
-   `open`
