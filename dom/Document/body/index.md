---
title: body
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Working Draft'
summary: 'Gets or sets the body element of the document.'
uri: dom/Document/body

---
# body

## Summary

Gets or sets the body element of the document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

``` {.js}
var bodyElement = document.body;
document.body = newBodyElement;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The [body](/html/elements/body) element of the document.

## Examples

``` {.js}
//get the document's body content, append to it, set new content
function appendBody() {
    var bod = document.body.innerHTML;
    bod += "<p>That's all, folks!</p>";
    document.body.innerHTML = bod;
}
```

## Usage

     Use this property to get the body element of the document, or to replace it with a new body element.

## Related specifications

Specification
:   Status
[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)
:   Recommendation
[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

