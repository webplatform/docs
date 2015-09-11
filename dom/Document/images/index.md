---
title: images
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
    value: ''
    href: /dom/Document
standardization_status: 'W3C Last Call Working Draft'
summary: 'Legacy method. Use document.querySelectorAll(&quot;img&quot;) instead. Gets a live collection of img elements in a document.'
tags:
  - API
  - Object
  - Properties
  - DOM
uri: dom/Document/images

---
## <span>Summary</span>

Legacy method. Use document.querySelectorAll(&quot;img&quot;) instead. Gets a live collection of img elements in a document.

Property of [dom/Document](/dom/Document)[dom/Document](/dom/Document)

## <span>Syntax</span>

**Note**: This property is read-only.

``` js
var imageCollection = document.images;
```

## <span>Return Value</span>

Returns an object of type<span></span>

A live collection of [img](/html/elements/img) elements in the document.

## <span>Examples</span>

Logging the source URL of the first image in the document using the legacy property.

``` js
// Caching the collection,
// instead of looking up the images property every time.
// Alternatively and more efficiently,
// use document.querySelectorAll("img") here instead.
var imageList = document.images;
// Verifying the collection is not empty.
if (imageList.length) {
  console.log(
    "The source URL of the first image in the document is - " +
    // Getting the src property of the first item in the collection.
    imageList[0].src);
}
```

## <span>Usage</span>

     This is a legacy property. Use document.querySelectorAll("img") instead, which returns a static list instead.

Use this property to get a live collection of [img](/html/elements/img) elements in a document.

## <span>Notes</span>

Since this property returns a live collection, there are performance implications.

## <span>Related specifications</span>

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#dom-document-images)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/dom.html#dom-document-images)
:   Last Call Working Draft
