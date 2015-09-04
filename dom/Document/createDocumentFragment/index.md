---
title: createDocumentFragment
tags:
  - API
  - Object
  - Methods
  - DOM
readiness: 'Almost Ready'
standardization_status: 'W3C Recommendation'
notes:
  - 'Needs compat table'
summary: 'Creates a new document fragment (DocumentFragment) object.'
uri: dom/Document/createDocumentFragment

---
# createDocumentFragment

## Summary

Creates a new document fragment (DocumentFragment) object.

*Method of [dom/Document](/dom/Document)*

## Syntax

``` {.js}
var documentFragment = document.createDocumentFragment();
```

## Return Value

Returns an object of type DOM Node.

The created DocumentFragment instance.

## Examples

``` {.js}

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

## Related specifications

Specification
:   Status
[DOM Level 3 Core](http://www.w3.org/TR/DOM-Level-3-Core/core.html#ID-35CB04B5)
:   Recommendation

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

