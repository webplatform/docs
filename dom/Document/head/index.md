---
title: head
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Candidate Recommendation'
notes:
  - 'Needs compat'
summary: 'Gets the head element of the document.'
uri: dom/Document/head

---
# head

## Summary

Gets the head element of the document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var headElement = document.head;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value">DOM Node</span></span>

The [head](/html/elements/head) element of the document.

## Examples

This example displays the text (innerHTML) of the document's `head` element.

``` {.html}
<!DOCTYPE HTML>
<html>
<head>
<title>New Document</title>
<meta name="Generator" content="Notepad">
<meta name="Author" content="Bob Palindrome">
<meta name="Keywords" content="document head">
<meta name="Description" content="head property example">
</head>

<body>

<p onclick="alert(document.head.innerHTML)">Click me to see the contents of the <head> element</p>

</body>
</html>
```

## Related specifications

Specification
:   Status
[W3C HTML5](http://www.w3.org/TR/html5/dom.html#dom-document-head)
:   Candidate Recommendation
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

