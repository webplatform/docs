---
title: 'body'
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
standardization_status: 'W3C Working Draft'
summary: 'Gets or sets the body element of the document.'
tags:
  - API_Object_Properties
  - DOM
uri: dom/Document/body

---
## Summary

Gets or sets the body element of the document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## Syntax

``` js
var bodyElement = document.body;
document.body = newBodyElement;
```

## Return Value

Returns an object of type DOM NodeDOM Node

The [body](/html/elements/body) element of the document.

## Examples

``` js
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

[DOM Level 2 HTML](http://www.w3.org/TR/2003/REC-DOM-Level-2-HTML-20030109)
:   Recommendation

[W3C HTML5](http://www.w3.org/TR/html5/)
:   Working Draft

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/)
:   Living Standard
