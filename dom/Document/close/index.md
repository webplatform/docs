---
title: close
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Closes an output stream and forces the sent data to display.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/close

---
## Summary

Closes an output stream and forces the sent data to display.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
 document.close();
```

## Return Value

No return value

## Examples

``` js
//open a new window/tab, open a new document in it,
//write to the document, and close the document (but not the window/tab)
function newWinDoc() {
    var win=window.open();
    win.document.open();
    win.document.write("<h1>Hello, world</h1>");
    win.document.close();
}
```

## Notes

When a function fired by an event on any object calls the [**close**](/dom/Window/close) method, the **window.close** method is implied. When an event on any object calls the ****close**** method, the **document.close** method is implied.

When [**document.write**](/dom/Document/write) or [**document.writeln**](/dom/Document/writeln) is used in an event handler, **document.close** should also be used.

## Related specifications

[DOM Level 2 HTML](http://www.w3org/TR/DOM-Level-2-HTML/)
:   Recommendation

## See also

### Related pages (MSDN)

-   `open`
