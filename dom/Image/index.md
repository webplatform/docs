---
title: Image
attributions:
  - 'Microsoft Developer Network: [[Windows Internet Explorer API reference](http://msdn.microsoft.com/en-us/library/ie/hh828809%28v=vs.85%29.aspx) Article]'
notes:
  - "Proper syntax and parameters\nhttp://www.w3.org/html/wg/drafts/html/CR/embedded-content-0.html#dom-image"
readiness: 'Almost Ready'
standardization_status: 'W3C Last Call Working Draft'
summary: 'Legacy. Use document.createElement(&quot;img&quot;) instead. Quickly constructs an img element.'
tags:
  - API
  - Objects
  - DOM
uri: dom/Image

---
## Summary

Legacy. Use document.createElement(&quot;img&quot;) instead. Quickly constructs an img element.

## Overview

A shorter legacy constructor for creating and loading images.

## Properties

*No properties.*

## Methods

*No methods.*

## Events

*No events.*

## Examples

The following script creates a new image and appends it to the **body** element.

``` js
var img = new Image(50, 50);
img.src = "image.png";
document.body.appendChild(img);
```

## Usage

     Use this constructor as a shorter way to instantiate new img elements before adding them to the document.

Syntax -

`new Image(width, height)`

You can specify up to two optional arguments:

||
|width|Optional. **Integer** that specifies the **img** width.|
|height|Optional. **Integer** that specifies the **img** height.|

## Notes

The loading process of the image starts as soon as its **src** property is set, even when not added to a document.

## Related specifications

[WHATWG HTML](http://www.whatwg.org/specs/web-apps/current-work/multipage/embedded-content.html#the-img-element)
:   Living Standard

[HTML5](http://www.w3.org/TR/html5/embedded-content-0.html#the-img-element)
:   Last Call Working Draft
