---
title: images
tags:
  - API
  - Object
  - Properties
  - DOM
readiness: 'Ready to Use'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Legacy method. Use document.querySelectorAll("img") instead. Gets a live collection of img elements in a document.'
uri: dom/Document/images

---
# images

## Summary

Legacy method. Use document.querySelectorAll("img") instead. Gets a live collection of img elements in a document.

<span data-meta="applies_to" data-type="key">Property of <span data-type="value">[dom/Document](/dom/Document)</span></span>

## Syntax

***Note**: This property is read-only.*

``` {.js}
var imageCollection = document.images;
```

## Return Value

<span data-meta="return" data-type="key">Returns an object of type <span data-type="value"></span></span>

A live collection of [img](/html/elements/img) elements in the document.

## Examples

Logging the source URL of the first image in the document using the legacy property.

``` {.js}
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

## Usage

     This is a legacy property. Use document.querySelectorAll("img") instead, which returns a static list instead.

Use this property to get a live collection of [img](/html/elements/img) elements in a document.

## Notes

Since this property returns a live collection, there are performance implications.

## Related specifications

Specification
:   Status
[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/dom.html#dom-document-images)
:   Living Standard
[HTML5](http://www.w3.org/TR/html5/dom.html#dom-document-images)
:   Last Call Working Draft

## Attribution

*This article contains content originally from external sources.*

Portions of this content come from the Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]

