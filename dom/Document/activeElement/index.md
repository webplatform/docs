---
title: 'activeElement'
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
readiness: 'Ready to Use'
relationships:
  applies_to:
    predicate: 'Property of '
    value: dom/Document
    href: /dom/Document
  return:
    predicate: 'Returns an object of type '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the &lt;body&gt; element.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/activeElement

---
## Summary

Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the &lt;body&gt; element.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

**Note**: This property is read-only.

``` js
var element = document.activeElement;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The currently active element of the document, or `<body>` if no element is active.

## Examples

``` js
//display tag name of currently focused element
function getActiveElement () {
    if (document.activeElement) {
        alert(document.activeElement.tagName);
    }
}
```

## Notes

The active element retains focus in the parent [**Document**](/dom/Document) even when focus is shifted from the parent to another application. If the focus returns to the parent **document**, focus also returns to the same active element.

## Related specifications

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

[W3C HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation

[W3C HTML5](http://www.w3.org/TR/html5/dom.html)
:   Candidate Recommendation
