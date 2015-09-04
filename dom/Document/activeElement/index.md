---
title: activeElement
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Candidate Recommendation'
summary: 'Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the <body> element.'
uri: dom/Document/activeElement

---
# activeElement

## Summary

Gets the object that has the focus when the parent document has focus. If no element in the document has focus, returns the \<body\> element.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var element = document.activeElement;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The currently active element of the document, or `<body>` if no element is active.

## Examples

``` {.js}
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

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
[W3C HTML5](http://www.w3.org/TR/html5/editing.html)
:   Candidate Recommendation
[W3C HTML5](http://www.w3.org/TR/html5/dom.html)
:   Candidate Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

