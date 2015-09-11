---
title: createDocumentFragment
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - 'Needs compat table'
readiness: 'Almost Ready'
relationships:
  method_of:
    predicate: 'Method of '
    value: dom/Document
    href: /dom/Document
  return_type:
    predicate: 'Returns an object of type  '
    value: 'DOM Node'
    href: /dom/Document
standardization_status: 'W3C Recommendation'
summary: 'Creates a new document fragment (DocumentFragment) object.'
tags:
  - API
  - Object
  - Methods
  - DOM
uri: dom/Document/createDocumentFragment

---
## <span>Summary</span>

Creates a new document fragment (DocumentFragment) object.

Method of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

``` js
var documentFragment = document.createDocumentFragment();
```

## <span>Return Value</span>

Returns an object of type DOM NodeDOM Node

The created DocumentFragment instance.

## <span>Examples</span>

``` js

var div, docFrag = document.createDocumentFragment(),  i = 0, thismany = 1000;

while ( i < thismany) {
    // Creates a new <div> element if one doesn't exist. Clones it if one does.
    (div === undefined) ? document.createElement('div') : div.cloneNode(false);

    // Appends div to the document fragment.
    docFrag.appendChild(div);

    i++;
}

// Appends the fragment and child nodes to the document body.  Makes one DOM update instead of 1000
document.body.appendChild(docFrag);

```

## <span>Related specifications</span>

[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-35CB04B5)
:   Recommendation
