---
title: write
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'In Progress'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs examples and compat'
summary: 'Method to insert a string of marked up text in the document tree.'
uri: dom/Document/write

---
# document.write

## Summary

Method to insert a string of marked up text in the document tree.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
 document.write(str);
```

## Parameters

### str

 Data-typeÂ
:   String

 A **String** that specifies the text and HTML tags to write.

## Return Value

No return value

**Needs Examples**: This section should include examples.

## Usage

     Do not use the write method or the writeln method on the current document after the document has finished loading unless you first call the open method, which clears the current document window and erases all variables.

## Notes

When [**Document**](/dom/Document).**write** or **document**.[**writeln**](/dom/Document/writeln) is used in an event handler, you must also use **document**.[**close**](/dom/Document/close).

## Related specifications

Specification
:   Status
[DOM HTML Level 2](http://www.w3.org/TR/DOM-Level-2-HTML/html.html#ID-75233634)
:   W3C Recommendation

## See also

### Related pages

-   `writeln`
-   `open`

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

