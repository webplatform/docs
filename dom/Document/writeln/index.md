---
title: 'writeln'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs summary, example, compat, better spec link'
readiness: 'In Progress'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Recommendation'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/writeln

---
**Needs Summary**: This article does not have a summary. Summaries give a brief overview of the topic and are automatically included on some listing pages that link to this article.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
 object.writeln(psarray);
```

## Parameters

### psarray

 Data-type
:   any

 A **String** that specifies the text and HTML tags to write.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Notes

### Remarks

In HTML, the carriage return is ignored unless it occurs in preformatted text. Do not use the [**write**](/dom/Document/write) method or the **writeln** method on the current document after the document has finished loading unless you first call the [**open**](/dom/Document/open) method, which clears the current document window and erases all variables. **Note**  When [**Document**](/dom/Document).[**write**](/dom/Document/write) or **document**.**writeln** is used in an event handler, you must also use **document**.[**close**](/dom/Document/close).

### Syntax

### Standards information

-   [Document Object Model (DOM) Level 2 HTML Specification](http://go.microsoft.com/fwlink/p/?linkid=196991), Section 1.5

## See also

### Related pages

-   `Reference`
-   write[write](/dom/Document/write)
-   open[open](/dom/Document/open)
