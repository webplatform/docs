---
title: head
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat'
readiness: 'Almost Ready'
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
summary: 'Gets the head element of the document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/head

---
## <span>Summary</span>

Gets the head element of the document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var headElement = document.head;
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The [head](/html/elements/head) element of the document.

## <span>Examples</span>

This example displays the text (innerHTML) of the document's `head` element.

``` html
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

## <span>Related specifications</span>

[W3C HTML5](http://www.w3.org/TR/html5/dom.html#dom-document-head)
:   Candidate Recommendation

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage)
:   Living Standard
